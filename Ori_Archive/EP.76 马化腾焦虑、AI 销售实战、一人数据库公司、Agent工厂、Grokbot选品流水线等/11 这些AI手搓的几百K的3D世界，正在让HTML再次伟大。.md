# 这些AI手搓的几百K的3D世界，正在让HTML再次伟大。

> 原链: https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647688394&idx=1&sn=a5db5eb7ca3dcd61d0774f97f3c2a5aa  
> 来源: mp.weixin.qq.com · 归档自 EP.76 · 抓取于 2026-11-20  

---

你要说上周用AI来做东西，最火的玩法是啥，那必然逃不过一个东西。就是用AI搓的纯HTML的3D游戏。![图片](https://mmbiz.qpic.cn/mmbiz_png/2jjfQoZLoqXPQcmFsNxrOpp3uqn5mob6XULBNL75Scce9dibviaLpIj5t75kiaibBIhLB71j4ebict8wR14zSaObZAqsDgfWwrJdOkBfub4icdiato/640?wx_fmt=png&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)不过呢，最离谱的一个，还是一个在各个群里疯传的究极小的HTML游戏文件，只要1.4M。![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/2jjfQoZLoqUQPic1wNRLQXc3eaF8BZ40SFqiaiaibeV8AuUvu44oqibAjWbsJObRK6QsDoMlDvHs8fyxAopNs9zwV1ItKURDYNfgwYfbk4MflUEg/640?wx_fmt=png&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=1)你只要下载下来，打开以后，你就会发现，这个画面的效果几乎是媲美很多的3A大作了。![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)没错，只要1.4M，你就可以玩到这样的游戏demo。不过这玩意不是原创，是把Anthropic的工程师Felix Rieseberg在Fable 5.2发布的时候他搓的代码，给纯扒下来汉化了一下，其他的原封不动，然后冠名国产3A大作。![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)不过这种行为我们就不说了，不是今天的重点。重点还是在于，我们所看到的文件大小，1.4M，因为在这个年代，手机512G都完全不够用、存储都已经比黄金还珍贵、随手一张相片都是十几M的情况下，一个1.4M的纯HTML游戏，下载下来，在浏览器里打开，就是这样的效果。这其实超出了很多人的认知的。当时群友很多都在讨论。。。![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)我就把这个文件代码打开来看了下，果然发现了一个很有趣的老朋友。Three.js。![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

这1.4M里，有将近一半，大概700KB，是一个叫Three.js的东西。

剩下的那一半，才是游戏本身。

因为没有用任何外部素材，所有的东西全部是代码直接写的，所以集装箱、吊机、雨、枪、光影、音效啥的，全都在剩下的700K里，没有一张图片，没有一个模型文件，连声音都是代码现场合成的，没有一段录音。

因为所有的东西都是代码，连模型文件都没有，所以实现了极限压缩。那我知道大家肯定想问，那Three.js到底是个啥？剩下这些东西，又是怎么塞进去的？我如果想做一个类似的这样的东西，我要怎么做？为了能让大家更好的理解，所以我们先极其简单的说一下，浏览器到底是怎么画3D的。

很多人可能不知道，你每天用的浏览器，本身就能直接调用显卡渲染3D的，靠的是一套叫WebGL的接口，这其实已经是2011年3月定下来的标准了，后来又有了新一代的WebGPU。

但这套接口，是给专业图形程序员用的，非常的原始非常的难用。

因为写的时候，你得手把手亲自告诉显卡，比如每一个三角形的三个顶点在哪，比如每一个像素的颜色怎么算，又比如光从哪个角度打过来，摄像机的位置和朝向，又要怎么换算成屏幕上的坐标。

究极神经病。

中间哪怕一步写错，你看到的就是一片黑屏，连个正儿八经的报错都没有，所以在在网页3D概念刚出来的那几年里，这一直是一小撮图形开发大佬的专属手艺活，其他的真没几个人能干的了这玩意。

直到，Three.js出现了。

![加描边后的图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

它干的活呢，就是把那些乱七八糟的东西，帮你封装成一个库，你不用再写之前给显卡直接看的那些神级代码了，你可以用一种极其简单的语言，来去在网页中创作3D。

你可以简单的理解成，它有点像网页上的一个轻量版游戏引擎。

做这个东西的人，叫Ricardo Cabello，一个西班牙程序员，网名Mr.doob。

2010年4月24号，他把Three.js的第一个版本传到了GitHub上。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

十六年下来，这个项目在GitHub上攒了11.7万个Star、两千多个贡献者，基本成了网页3D的事实标准。

这1.4M里的那七百KB，就是把整个Three.js原样打包进了文件里。

那剩下的一半，凭啥能装下一整个游戏的demo呢。

答案是，这些东西，根本就没有被存在文件里，这是一个很有趣的思路。

我简单举个例子。

假设你要给朋友描述一个人。

一种办法，是拍张照片发过去，照片里每一个像素的颜色，你就都存在文件里，一模一样，所以照片极大。

另一种办法，你直接给朋友发一条微信，说：“一个很帅的男人，头发中分，左右各一半，刘海梳得特别顺，穿一身背带裤，两根带子挂在肩上，手里拍着一个篮球。他先对着镜头自我介绍，说自己练习时长两年半，爱好是唱、跳、rap、篮球。”

朋友看着这条微信，不用你发一张图，自己绝逼就能把这个人直接渲染出来。

第一个方式，可能是10M的大小，而第二种方式，可能只有1k不到，这就是差距，可能差了几万倍，但是对于最后的终点来说，传达的信息，是差不多的。

所以呢，你的文件里存的其实并不是集装箱长啥样子，本质上是一段告诉浏览器怎么生成这些集装箱的代码，雨也一样，存的不是雨，是雨点从哪落、落多快的规则，贴图、声音，全是这个套路。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

所以你会发现，你第一次打开游戏的时候，有这个东西。

这套做法，有个专门的名字，叫程序化生成。

所以硬要用一个比喻的话，就是你打开的那个HTML文件，其实是一份菜谱，不是一盘已经做好的菜。

真正的菜，是你打开网页的那几秒钟里，你自己电脑的显卡，现场直接给你炒出来的，显卡现炒，匠心制作。

这也是为什么这类网页打开的时候，经常要等几秒，有的电脑风扇还会呼呼转一下，那几秒，就是显卡在给你生成整个世界。

当然，1.4M还不是最小的，如果你还想往下压，也可以。

比如这个很屌的水世界。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

一共97K，纯HTML，直接连Three.js都没有，直接Claude Fable 5.2手搓源码，直接用WebGPU渲染。

过于吓人了。

感觉已经很久没有多少人在乎大小了，在现在动不动一个APP可能1、2个G的情况下，在AI的加持下，居然开始有人回到了很久以前，玩极限压缩的挑战。

而且，这种能力，现在因为AI，开始属于每一个人。

AI让HTML再次伟大。

那简单的教大家一下怎么生成一些有趣的3D网页。

首先肯定是模型，王中王自然是Claude Fable 5.2了，这个在审美上目前是断档领先的，并且在性能上也几乎能压缩到极致。

但很多人肯定没办法用Claude，那其实用Gemini 4 Carbon和GPT-6 Astra也能跑，DeepSeek V4.1 Flash的效果也还凑合，只不过改起来就要费点心了，肯定没有Claude Fable 5.2那么省心直出。

然后Prompt其实也非常简单，大白话就可以了，为了效果起见，我的建议还是尽量调用Three.js，没事别为了极限压缩去挑战地狱难度，Claude Fable 5.2可以，不代表其他模型也可以...

所以我简单搞了一个模板。

  *   *   *   *   *   *   *   * 

    
    
    帮我做一个单文件的HTML网页，用Three.js实现一个可以自由浏览的3D场景。场景是：【你想要的画面，越具体越好。比如：重庆洪崖洞的夜景，层层叠叠的吊脚楼亮着暖黄色的灯，前面是嘉陵江，江上有游船，旁边是千厮门大桥，远处是城市的楼群】要求：1.所有模型和贴图都用代码生成，不要引用任何外部的图片和模型文件。2.支持鼠标拖动旋转视角、滚轮缩放。3.画面要有氛围感，重点处理光照、雾气和色调。4.在普通的笔记本上也要流畅，加载的时候显示进度。5.主要物体，都做成独立的组件，方便我后面单独修改。

里面最重要的是第1条，不要用任何外部的图片或者模型文件，这样方便，体积也小。

第5条是个小技巧，尽可能解耦，一开始就拆成独立组件，这样后面想把某栋楼改高一点、把桥换个颜色，就不会牵一发而动全身。

这是我们简单的用类似的提示词，让GPT-6 Astra跑出来的洪崖洞。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

洪崖洞层层叠叠的吊脚楼、旁边的千厮门大桥、前面的嘉陵江和游船，还有背后的城市楼群，基本都被搭了出来。

而Three.js的能力其实有很多，你也可以用它，来搞交互。

比如我有又随手用它做了一个3D的可以玩的魔方。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

你也可以用它，来做动画，比如这两天X上爆火的一个90秒的片子。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

完全由Three.js生成，我一定要让大家看一下这个效果。

![]()

已关注

__

关注

__ 重播 __ 分享 __ 赞

关闭 __

**观看更多**

更多 __

__

__




__

_退出全屏_

 __

_切换到竖屏全屏_ _退出全屏_

数字生命卡兹克已关注

 __

分享视频

 __，时长 01:25

0/0

00:00/01:25

切换到横屏模式 

继续播放

进度条，百分之0

 __

播放

00:00

/

01:25

01:25

倍速

 _全屏_

 __倍速播放中

0.5倍  0.75倍  1.0倍  1.5倍  2.0倍 

超清  流畅 

您的浏览器不支持 video 标签 

__

继续观看

这些AI手搓的几百K的3D世界，正在让HTML再次伟大。 

观看更多 __

转载

,

这些AI手搓的几百K的3D世界，正在让HTML再次伟大。

 __

数字生命卡兹克 已关注

分享点赞推荐在看

 ____已同步到看一看写下你的评论

 __

视频详情 

虽然最后渲染成了一个视频，但是它本质，可是一个HTML哦，而且，是只有2M的HTML哦，打开以后，直接给你实时渲染播片。

![加描边后的图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

我很久没有看到这么让人爽的东西了。

而且，Three.js做流体效果也是一绝。

![]()

已关注

__

关注

__ 重播 __ 分享 __ 赞

关闭 __

**观看更多**

更多 __

__

__




__

_退出全屏_

 __

_切换到竖屏全屏_ _退出全屏_

数字生命卡兹克已关注

 __

分享视频

 __，时长 02:01

0/0

00:00/02:01

切换到横屏模式 

继续播放

进度条，百分之0

 __

播放

00:00

/

02:01

02:01

倍速

 _全屏_

 __倍速播放中

0.5倍  0.75倍  1.0倍  1.5倍  2.0倍 

超清  流畅 

您的浏览器不支持 video 标签 

__

继续观看

这些AI手搓的几百K的3D世界，正在让HTML再次伟大。 

观看更多 __

转载

,

这些AI手搓的几百K的3D世界，正在让HTML再次伟大。

 __

数字生命卡兹克 已关注

分享点赞推荐在看

 ____已同步到看一看写下你的评论

 __

视频详情 

当然，你觉得纯代码做出来的模型不够精细，特别是人、动物这种曲线多的东西，也可以用Blender、Tripo先把模型做好，再让AI放进网页里。

不过这样体积就会大一点了，但是Three.js也支持这么玩，没有任何问题。

然后很多时候，因为模型的审美和能力确实不够，所以要改很多轮才能效果比较好，那这个时候，我也给大家分享一个我自己常用的一个小方法。

就是直接让模型审自己。

加一句Prompt就行：

  *   *   * 

    
    
    每改完一版，用浏览器打开它，从几个固定的角度各截一张图。再开一个子Agent，只给它看截图，不给它看代码，让它以一个挑剔的美术指导的角度，按严重程度列出画面问题。你按它的意见改，一直改到它只剩小问题为止。

这样它就会自己去迭代很多轮，然后一直把效果打磨到最优。

大概就是这样。

最后，我知道可能很多人会问，用AI生成这种3D的HTML玩意，有什么用？

说实话，你从商业上来说，可能确实没啥大用。

但这世间所有事情，也都并不是功利的。

它让我看到了一种久违的浪漫。

在很长一段时间里，做出一个逼真的3D世界，那是巨头工作室的特权，是几百人团队熬上几年才能磨出来的艺术品。

你我这样的普通人，脑子即使里有再宏大的山河，也是巧妇难为无米之炊。

但现在，那道高不可攀的墙塌了。

几百K的代码，一个最朴素的浏览器，每个人都能在自己的桌面上，当一回造物主。

这可能，就是技术最迷人的时刻吧。

******以上，既然看到这里了，如果觉得不错，随手点个赞、在看、转发三连吧，如果想第一时间收到推送，也可以给我个星标⭐～谢谢你看我的文章，我们，下次再见。******

>/ 作者：卡兹克、可达

>/ 投稿或爆料，请联系邮箱：agent@virxact.com
