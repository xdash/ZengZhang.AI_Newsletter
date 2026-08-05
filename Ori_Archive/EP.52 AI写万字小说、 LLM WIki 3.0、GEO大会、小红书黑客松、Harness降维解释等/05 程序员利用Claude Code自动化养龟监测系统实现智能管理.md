# 程序员利用Claude Code自动化养龟监测系统实现智能管理

> 原链: https://www.huxiu.com/article/4849810.html?f=rss  
> 来源: 叶水水 · 归档自 EP.52 · 抓取于 2026-08-05  

---

本文来自微信公众号： [少数派](https://mp.weixin.qq.com/s?__biz=MzU4Mjg3MDAyMQ==&mid=2247611689&idx=1&sn=377ba9af569af2dfb2e26d4f609bf1ae&chksm=fc7541a7e2d36d1da37675a8455f400382bb9bfe326e6c50f0b03c06c180b1d8732e76eaba4d#rd) ，作者：叶水水，原文标题：《程序员养龟有多离谱？我让 Claude Code 每天给我发乌龟行为报告》

## ▍背景

最近对养龟产生了兴趣，家里陆续来了6只：草龟、地图龟、西非侧颈龟、三只黄喉拟水龟。龟缸上装了TP-Link摄像头，群晖NAS跑着Surveillance Station 24小时录像，水温传感器和加热棒也配齐了。

东西都有，但用起来全是分散的。看温度一个APP，看摄像头另一个，加热棒手动开关。录了几百GB的视频从来没人翻。

刚好最近一直在用Claude Code折腾家里的Home Assistant，上周才用它逆向了空气净化器的API。这次想试试，纯靠对话，能把养龟这件事做到什么程度。

## ▍现在是什么样的

打开手机HA，龟缸的东西全在一个页面里，摄像头画面、乌龟活动状态、加热棒功率和用电量、水温湿度趋势。温度异常会聊天软件推送。

每半小时还会收到一段精华视频和一段AI写的行为分析：

![](https://img.huxiucdn.com/article/content/26-04-12/91ebd74f-57c1-480e-9d6a-9b0510a63ae2.png?imageView2/2/w/1000/format/png/interlace/1/q/85)


![](https://img.huxiucdn.com/article/content/26-04-12/2e7fa990-0673-4417-88ef-1a0161a0112e.png?imageView2/2/w/1000/format/png/interlace/1/q/85)


整个过程我没写一行代码。仪表盘、自动化、监控脚本、视频处理、AI分析，都是和Claude Code聊出来的。

## ▍HA仪表盘和自动化

跟Claude Code说的第一句话大概是「把乌龟摄像头加到HA仪表盘上」。

然后就是不停地提需求：

「加热棒的功率和用电量也显示出来」

「水温做个仪表盘，标出适宜温度区间」

「加个24小时和7天的水温趋势图」

「温度太低或太高给我发消息」


它每次直接改HA的配置文件和仪表盘数据，改完重启，我刷新手机看效果。不满意继续说，满意就下一个。跟一个懂HA的人聊天没什么区别，我不用管YAML怎么写、automation怎么配。

![](https://img.huxiucdn.com/article/content/26-04-12/4fbaf298-1a36-42ad-aea9-436c6a776908.png?imageView2/2/w/1000/format/png/interlace/1/q/85)


![](https://img.huxiucdn.com/article/content/26-04-12/384c4fd3-f084-442d-9ea4-d0a0a4d8b1e0.png?imageView2/2/w/1000/format/png/interlace/1/q/85)


左：加热棒7天功率、水温湿度仪表盘；右：24小时水温湿度趋势，带温区标注

水温趋势图标了过冷/偏冷/适宜/偏热/过热的区间。加热棒功率曲线能看出工作规律，比如图上4月7号之前加热棒是关着的，之后才开始工作。

自动化跑了温度过高和过低两条告警。温度异常聊天软件几分钟就能收到。

## ▍AI活动监测

仪表盘能看数据了，但龟在干嘛，水温曲线看不出来。

我问Claude Code能不能做个活动监测。它的方案：每5分钟从SS录像里抽帧对比，检测画面变化判断龟有没有在动。处理放在家里闲置的Mac 16"（M1 Max 64GB）上，NAS只管存录像。

## ▍抓帧对比

录像在NAS，Mac通过SSH读取。一开始传整个100MB的mp4，12秒。后来只传文件头5MB（mp4的moov atom在文件头，够解码出帧），降到2秒。

NAS录像→ssh head-c5MB→OpenCV读帧→灰度+高斯模糊→像素差值


变化超2%就算「活跃」，结果推到HA sensor。

## ▍精华视频

「有活动时直接发视频给我」

Claude Code做了每30分钟的精华视频。检测到活跃的时间点，从对应录像截取片段拼在一起。

一个细节：一开始用OpenCV逐帧重编码，25秒出一个片段，画质还糊。后来装了ffmpeg用-c:v copy直接裁切，2秒搞定，1080p原始画质。工具选对了差十倍。

## ▍本地大模型看龟

精华视频解决了「看什么」。但我还想知道每只龟在干嘛。

我问有什么办法识别不同的乌龟。Claude Code列了几种：OpenCV颜色轮廓检测、YOLO、深度学习个体识别、Vision LLM。6只龟品种差异大，草龟最小深色、地图龟最大有花纹、西非侧颈脖子侧扁、小青体型差不多，直接用视觉大模型就行，不用训练。

试了Gemini API配额不够。我说能不能跑本地的。最后用Ollama跑Gemma 4（8B Q4量化），M1 Max 64GB没什么压力。

分析分两步。先逐帧：从30分钟录像均匀抽30帧，每帧单独让Gemma描述看到了什么。再汇总：30条描述拼一起，让Gemma总结这半小时。

prompt改了好几轮。一开始让它「分析哪只最活跃哪只最安静」，输出很八股。我说不关心这个，改成「像朋友聊天一样说说」，输出就对味了。

## ▍架构

HA管数据采集、展示、告警。Mac管视频处理和AI推理。两边通过HA REST API连起来。launchd定时跑，开机自启。


![](https://img.huxiucdn.com/article/content/26-04-12/e865a3e2-e326-473f-89e5-def04476fa4c.png?imageView2/2/w/1000/format/png/interlace/1/q/85)


## ▍关于没写代码

系统里有Python脚本（OpenCV图像对比、ffmpeg调用、Ollama API、Telegram通知）、HA的YAML配置（sensor、automation、lovelace dashboard）、launchd定时任务，代码量不算少。

但我确实一行都没手写。

每一步都是对话完成的。我说「把摄像头加到仪表盘」，它改lovelace JSON。说「温度告警发聊天软件」，它写automation YAML。说「用本地模型分析龟缸画面」，它装Ollama、拉模型、写脚本、配定时任务。

我干的事更像是产品经理：说需求、看效果、给反馈。

不是说技术不重要了。这套系统里有不少技术判断，比如只传mp4头部5MB而不是整个文件、用ffmpeg stream copy而不是重编码、逐帧分析再汇总而不是多图一起扔给模型。只是这些判断现在AI也能做。

## ▍成本

几乎为零。硬件家里都有，软件全开源，AI推理跑本地。Mac每月多费大概3块钱电。

养龟是个慢节奏的事。但每天翻翻聊天软件的报告，看看谁又霸占了晒背台、谁偷偷换了个位置，比蹲在缸前看半天有意思多了。
