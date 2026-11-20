# 卡兹克的 Agent-Autoloop 我又跑了一周：加了中控台，接进了公司真实业务

> 原链: https://mp.weixin.qq.com/s?__biz=MjM5ODQ3MDk0Mg==&mid=2448912486&idx=1&sn=1c624db5497bc833722f1808d2bbd546&chksm=b3f10d8880c08bb0ecb1b353de4eb8e863b7f59f5789c7ab1e01168445a86cbcefb253d61588&mpshare=1&scene=1&srcid=1116rv2LTZsJzm6Nkwf54mUb&sharer_shareinfo=c72c128193f68b83ce47ed1bbf90dd3e&sharer_shareinfo_first=c72c128193f68b83ce47ed1bbf90dd3e  
> 来源: 公众号 · 归档自 EP.76 · 抓取于 2026-11-20  

---

测试同事在飞书表格里写一行问题，Agent 接单、修改、审查，我点两下，状态自己写回表里。

上一篇写了我怎么用卡兹克开源的 Agent-Autoloop，把自己的小项目跑成自动流水线。没想到有 6000 多阅读。写完之后，我自己也一直在想两个问题：**看不见它在干什么，敢放手吗？公司的真实业务能用吗？**

这一周我就围着这两个问题做了升级。先说结论：**加了一个中控台，把入口从“群里一句话”换成了“飞书问题表”，然后接进了公司的一个真实项目，测试同事提的问题已经在这条流水线上跑了。**

![图片](https://mmbiz.qpic.cn/mmbiz_png/kic9r3fpKMlBenZtlCwNVcpIhV4ibZ4b9s0kOziaUWv4j3ibPGQu04fHOtBiaWCibW6GLNkYIbFxET6GRsTuDQH3G6sibib4SpBapnbWesWHmPV0BOI/640?wx_fmt=png&from=appmsg&watermark=1&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)

图 1 · 相比上一篇，这次升级的四件事

## 一、先看全貌：一单是怎么走完的

下面这张动图是中控台里的“全景图”，点一下“演示”，它会把一单从提出到关闭走一遍。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 2 · 全景图（动图）：一单从提出到回写，光点走到哪，上方就讲到哪

**所有交接都经过中台。** 每个 Agent 干完，把结果交回 Agent-Autoloop，中台按规则交给下一个。Agent 之间互不认识，换模型、加环节只是改规则。

**能用脚本的地方不叫醒模型。** 接单、跑测试、提交推送、回写表格都是脚本，只有派单、编码、审查、验收这四处才用 Claude 和 Codex。

**人只在橙色的地方出现。** 确认新问题、点“合并并推送”、发布后点“已发布”。

## 二、中控台：终于不用翻终端了

上一篇里，想知道某一单走到哪了，得去终端里敲命令。单子一多就很烦，于是让 Agent 给自己做了一个网页。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 3 · 中控台总览：什么在等我、每单走到哪、花了多少，一眼看完

点进任意一单，是它的完整时间线：谁干了什么、用了多久、花了多少钱、交给了谁，我在哪张卡片上点了什么。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 4 · 一单的真实时间线（长图）。橙色的两块是我点过的卡片

除了看，项目、规则、各个 Agent 的约定手册，也都能在这里改。

## 三、飞书：从“群里一句话”到“一张问题表”

自己的小项目，在群里发一句“需求：xxx”就够了。公司的项目有测试同事，问题一天好几条，还要知道每条的状态，群聊干不了这个。所以入口换成了**飞书多维表格** ：测试同事一行写一个问题，带上描述和截图。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 5 · 表格既是入口，也是看板：中间几步的状态是流水线自己写回去的

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 6 · 飞书里的真实问题表：左边是测试写的问题，“状态”和“处理说明”是流水线写回去的

围绕这张表，飞书里有四种交互：

**新问题先问我。** 机器人私聊提醒我，我把状态改成“待处理”，流水线才接单。Agent 不会自己决定修什么。

**每单一条进度消息，原地更新。** 从接单到验收，私聊里始终是同一条消息在变，不刷屏。

**几单合成一张卡片问我。** 几分钟内审查通过的单子，合成一张“合并并推送？”卡片，我点一次就都推了。之后我在 Jenkins 发布完点“已发布”，才开始验收。

**没修好，改一下状态就行。** 测试把这一行改成“复验不通过”，补上哪里没过，同一单自动重开，带着上一轮的记录返工。

## 四、真实业务跑得怎么样

接进来的是公司的一个支付 SaaS 项目，前端、后端两个仓库。加上原来的小项目，现在是三个项目共用一套流水线。

这周测试同事提的问题里，有 7 条进了流水线：**1 单测试已经复验通过、关闭了，3 单修完在等复验，2 单在等我推送或发布，1 单派单看完代码判断“不是问题”，说明原因后直接关了。** 有的问题同时涉及前端和后端，就拆到两个仓库各走各的流程。

挑其中一天中午的两单说说。两个都是界面上的小问题：一个是点了按钮后弹窗没关，一个是报告里几个按钮点了没反应。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

图 7 · 两单的真实时间线：蓝色是 Agent，橙色是在等我

从接单到验收完一共 37 分钟，Agent 实际干活约 10 分钟，其余是在等我点卡片、去发布。两单的审查都是一次通过，模型费用分别是 1.14 和 2.35 美元。放到整周看：最近 7 天真正干了活的有 322 轮，有记录的模型费用约 36 美元。

**也有不顺的地方。** 验收 Agent 原来看不到登录后的页面，只能核对代码。这周给它加了“只看不改”的浏览方式：自己登录测试环境看页面，会改数据的请求一律拦下。但这两单的页面，查询接口恰好不在放行范围里，数据加载不出来。它没有硬闯，也没有装作看过，而是如实写了“只核对了代码，请测试复验”，并把复验步骤逐条列给了测试。放行范围当天就补上了。

所以修没修好，最后还是测试同事说了算。另外 3 单的复验结果，下一篇再报。

## 五、三点新体会

**入口要选团队本来就在用的东西。** 测试同事不需要知道背后有 Agent，照常在表格里写问题、看状态就行。流水线去适应人。

**看得见，才敢放手。** 中控台没有让 Agent 更聪明，但我知道了每一单在哪、卡在谁手里、花了多少，才敢把公司的项目接进来。

**给 Agent 眼睛，但别给手。** 验收能登录测试环境看页面，但只能看；推送要我点，发布我自己来。看不到的就如实说，这一条写进了每个 Agent 的约定里。

## 写在最后

上一篇我说，变的不是模型，是组织方式。这一周的感受是：**组织方式一旦搭起来，往里加人、加项目、加环节，都比想象中容易。** 从一个人的小工具到团队的真实业务，框架一行没改，改的都是规则、脚本和约定。

再次感谢卡兹克，把 Agent-Autoloop 开源出来。它的内核足够小，边界足够清楚，才让这些扩展成为可能。

项目地址：

https://github.com/KKKKhazix/agent-autoloop

如果你也在用，欢迎留言交流。觉得有用的话，点赞、在看、转发，也去给卡兹克的项目点个 Star。
