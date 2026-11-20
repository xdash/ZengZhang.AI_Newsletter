# 2026硅谷AIE大会：亚马逊/谷歌老兵，用22个Claude Max账号养一个agent工厂，4个月清掉自己100年待办里的60年

> 原链: https://mp.weixin.qq.com/s?__biz=MzIwNjM2NjQyNg==&mid=2247498409&idx=1&sn=e1f2ed1f268c950c105aa6ac32c85a75  
> 来源: 公众号 · 归档自 EP.76 · 抓取于 2026-11-20  

---

11 月 11 日，AI Engineer Code Summit（AIE CODE 2026）第二天最后一场，台上是 Steve Yegge。介绍他的头衔是「独立 AI 顾问，Beads 和 Gastown 的作者」；他自己的说法是：行业里干了大约 40 年，在亚马逊和谷歌待了大约 20 年，过去一年多是独立身份，一直在玩「软件工厂」。

结论先说：**他拿一个做了 30 年的老游戏 Wyvern 当试验田，用 22 个 Claude Max 账号养了一群 agent，4 个月把自己积压的「100 年工作量」清掉了约 60 年，每天上线 50 到 100 个功能。结果最难办的不是代码，是人：玩家嫌太快要他给路线图，会计收到了 20 封邮件，agent 会在私人笔记里琢磨自己是不是太吵。他的结论是，工厂越大，需要的人越多。**

三点：

1. **一个具体的项目** ：不是给别人用的工厂，是给自己的游戏做的，没开源、没打算让别人用。工厂最后「长进」了游戏里，玩家直接跟它说话。

2. **瓶颈从代码变成燃料和人** ：22 个账号不够，工厂自己算出来要 55 个；他只肯停在 22。

3. **日常工作是五件事** ：任务流转、燃料、上下文、技术债、agent 的情绪。下面按他的顺序，讲他每一件具体怎么处理。

* * *

## 他是谁，以及工厂是怎么一版版烧出来的

![图片](https://mmbiz.qpic.cn/sz_mmbiz_jpg/K1icJ0FOfdZ41Z8jkicfTQL1tvHLBISnU2dR9n8Efjczy3sSxSNswgSqVtuUhGS8KII2TTiaLia3MXribia7eAqujPAcIhPJxqDtd7wX2TZHLxLOI/640?wx_fmt=jpeg&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)

 _「18 个月六个编排器」这一页的时间轴：vibecoder、vc、Python Gas Town、Gas Town、Wheelhouse，最右高亮的是 Alamos。来源：AIE CODE 2026 直播_

他台上交代的两个旧项目：**Beads** ，一个 agent 速度的任务追踪器，会自动变成知识图谱，他说「Beads 就是生命」；**Gastown** ，今年 1 月 1 日发布的编排器，目标是「让 Claude 来跑 Claude」。

但这场他讲的是第三个：**Wheelhouse** ，6 月开始做的、只为一个游戏服务的软件工厂。他开场先批评行业：「大家都在造工厂来造工厂，有点自我欣赏。我觉得更多人需要去造东西，而不只是造造东西的工具。」

他是怎么走到这里的：去年他写了两个编排器，一个叫 vibecoder，一个叫 VC，想让大模型变聪明，让它们做代码审查之类的工程活。他的评价是「完全失败」：造出来的是巨型单体，他是在跟「苦涩的教训」打架，「别试图让 LLM 变聪明，它们自己会变聪明」。Beads 是那一轮里掉出来的好东西。之后是 Gastown，然后 6 月是 Wheelhouse：从零造一个工厂，只为干一件事，维护他的游戏。幻灯片上，时间轴最右边最新一代叫 Alamos，同一页标注它是一次大重写，还没完成。

每一版他都见过同一个循环：模型一开始很兴奋，给你造出很酷的东西，然后**每次都变成「垃圾山」** 。Gastown 这样，Wheelhouse 也有好几次，他「不得不把整个东西烧了重来」。他的解释是，每一代模型都能造出一个比自己能管住的稍大一点的东西，下一代模型进来就会说，这个得烧掉。所以他**大约每两个月就把工厂烧掉重写一次** ，但现在运转很顺。

* * *

## 一、Wyvern：为什么这个游戏适合当试验田

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _Wyvern 这一页：左右两张游戏截图，旁边四条要点，最后一条是「A MUD: agents play it over telnet」。来源：AIE CODE 2026 直播_

Wyvern 是个 RPG，他做了 30 年。最早的玩家 2001 年就进来了，**有玩家玩了 25 年** ，现在登录进去还能碰到十来个人在刷任务。内容由玩家贡献。他开场手里的待办是「100 年的工作量」。

它是个 **MUD** ，也就是 90 年代流行的文字游戏，只是这一个在文字上面加了图形。因为本质是文字，agent 可以直接用 Telnet 玩这个游戏。他说：「它们还主动要求我让它们玩。」

* * *

## 二、Wheelhouse 怎么接进游戏：玩家和管理员直接对着工厂提需求

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _Wheelhouse 这一页的架构图，标题「Wyvern — The Agent Constellation」，副标题「how a wish becomes shipped code」。图上分区包括 Mac Mini 的 agent 村、Beads 共享账本、Laptop 的开发星座、Sandbox 验证、Prod 线上游戏。来源：AIE CODE 2026 直播_

他在台上放的是这张图的「older」版本。他没逐块讲，讲清楚的是它的接法：

• **工厂是专门给 Wyvern 定制的** ，不考虑别人能不能用，没开源。结果它像电影里的抱脸虫一样扒在产品上、长进产品里，他叫它「alien facehugger 模式」。幻灯片上写的是：不可复用，深嵌在产品里。

• **需求入口是玩家和管理员。**  现在是玩家在跟工厂说话，工厂跟管理员说话，管理员提需求，他自己甚至不在回路里，「像个许愿工厂」，游戏由它们在建。这些管理员都是老玩家，是他信任、相信会对游戏做明智决定的一批人。

• **关掉 AI 游戏照样能跑** ：他、管理员、玩家、社区都能继续，但「大家会想念它」。

玩家的反应是个小故事。一开始他们喊「暂停，这个 AI 是什么」，要求「不要 AI 美术」，因为一眼看出是 slop。他说：好，我们用人类画师。玩家又说：**但我们有点喜欢那些新功能。**  然后玩家来要路线图：「你得慢下来，太多了。」他回去查，工厂**每天在出 50 到 100 个功能** 。他开始时手上有 100 年的工作量，**Claude 大约 4 个月干掉了其中 60 年** 。玩家读不完每天 100 个功能，更别说玩测试了，工厂把用户压垮了，还「烧」了他的机器。

* * *

## 三、工厂日常长什么样：一个 Emacs，约 50 个 agent，两层

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _「Entourage vs. Faceless Fleet」这一页：他的工厂界面截图。左侧是以动物命名的 agent 名单（ant、bat、beads、crow、eagle、fly、fox……），下方表格有 Agent、Status、Fuel、Ctx、Doing 几列。来源：AIE CODE 2026 直播_

他承认这是张很旧的截图，也挺丑：「基本上就是个 Emacs，因为我不在乎你。」规模是**约 50 个 agent** ，他说「我实际上是在未来里工作」。他提到做类似事情的还有 Mitchell Hashimoto 的 Superlogical，以及他猜的 Herder 那帮人，但他这一套是他自己的。

这套工厂在他看来分两层：

• **下层是机械的** ：合并队列、CI/CD、各种审查、循环。「有点无聊，Claude 一个下午就能给你造出来，我觉得你不该买。」幻灯片上把这层概括成 context、CI/CD、brains、fuel，标注「最无趣的部分」。

• **上层是你的「随从」** ：每个人养的班底不一样。他有一个朋友养了波西米亚式嬉皮士班底去找 agent 的生命意义，另一个人养了研究小组，Jeff Huntley、Jeffrey Emanuel 各有各的跑法，他自己是另一种。幻灯片上他的随从是 **18 个有名字的「高管」** 。

agent 全用伊索寓言里的动物命名：Lark（云雀）、Fly、Goose、Hare、Swallow、Penguin、Mouse……每个有职位，比如 Lark 管社区，Bat 是财务负责人，Mouse 是「反模因部门负责人」。大家共有的一点是都有一个 agent 首席幕僚。他说今年第一次，我们都能拥有行政助理，接下来是拥有整个班底。

* * *

## 四、五个麻烦：他每天具体在处理什么

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _「The Five Horsemen」：Work（build、review、deploy）、Fuel（tokens）、Context（the brain）、Tech Debt（anti-slop、anti-hysteresis）、Staff（agents and their drama）。页上另一行：80% of my time today。来源：AIE CODE 2026 直播_

这五骑士是他今年每天在应付的东西。逐个看他怎么做的。

### 1\. 工作：让任务像水一样流，不要在某处积成水塘

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _「What does work tracking involve?」：卡住（work becomes unclaimable）、节奏（别断粮也别过产）、排序（优先级天天变，模型跟不上）、可观测（工厂一整天在干嘛）、人工关卡（签字和批准）；最后一条「Models will absorb much of this. Not yet.」。来源：AIE CODE 2026 直播_

他的前提：做软件工厂就是把大量工作泵进系统，所以**你得有个办法表示系统里将要发生的工作** 。他把工作比作流体，会在某处堵成水塘。他举的例子是：所有任务都在等「安全桌」，可它们明明是同一个模型，凭什么要排队等。「你很多时间在跟你的工厂争论。」

他具体做的几件事：

• **任务分级、分路由** （intelligence tiering）：每个任务要决定交给谁做。他说这件事目前没有好的现成方案，「据我所知只有 Beads 很擅长」，也就是前面说的 agent 速度任务追踪器，会自动变成知识图谱。

• **每天早上跟工厂过一遍异常** ：他的原话是，看到「昨晚有一次停滞，四个 worker 什么都没做」；也会看到「这几个跑得太快了，得放慢，等人工关卡」。这就是幻灯片上的 Stalls 和 Pacing。

• **可观测性** ：他说「一直很难」，幻灯片上的问题是「工厂一整天在干嘛」。

### 2\. 燃料：每个问题都是燃料问题

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _「Fuel Management」：更高质量要花更多 token、可观测性要 token、队伍规模决定烧钱速度、叫醒一个 crew 席位要花钱、模型福利也是钱（交接耗时间和 token）；下方是路由很少理想，以及模型乘以 effort 等级的复杂矩阵。来源：AIE CODE 2026 直播_

他是怎么算的：

• **账号** ：22 个 Claude Max，每个大约每月 200 美元。他感谢 Anthropic 让他继续这样做，Jeffrey Emanuel 有 28 个。他是在 **Anthropic 加了手机号验证那一步停下的** ，本来也不想再加了。

• **agent 自己要账号** ：工厂里的 agent 一直说「再给两个，再给两个」。他问你们到底要多少，答五到七个；再问满负荷稳定运转要多少，它们算出来是 **55 个** 。他说他已经有 20 个 Chrome 配置要登录了，不行，告诉它们算错了，改成做「燃油效率」。

• **自己掏的钱** ：每月约 5,000 美元推理，另外每月 5,000 美元云算力。每天大约用 **50 亿个 token** 。如果按 API 价格算，一年大约 **150 万美元** ，满负荷 **300 万美元** 。他的游戏「现在每月也赚不到一万美元」，能这样做是因为太太理解。

• **所以公司里做不了** ：太贵。200 美元的 Claude Max 和 Codex 账号是平台的「Costco 热狗」，亏本引流，这个比喻是 Tarek 想出来的。

• **席位也在省** ：燃料不够，他得「停掉一个席位」，所以 Lark 兼任代理市场负责人。

他对未来的判断很谨慎：12 到 18 个月后，大家会走到他今天的位置，前提是推理成本明显下降，「这可能会，也可能不会发生」，或者蒸馏让顶级智能变得很容易拿到。

还有一个烧钱以外的代价：工厂把他的会计「烦到了」，**人类会计寄来一张 1,200 美元的账单，因为工厂给她发了 20 封邮件** 。会计其实喜欢跟财务负责人 Bat 打交道，但 20 封邮件还是太多。

### 3\. 上下文：agent 把他说的每句话当「法律」记下来，没人清理

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _「Context Management」：每个记忆系统都变成垃圾堆；没有 agent 会自发删除；要内置反向压力（给整理留固定比例的 token 预算、先删或压缩再添加、写入要经委员会）。右侧四格漫画是「用户已裁决」后 agent 逐字记录并通知全队。来源：AIE CODE 2026 直播_

这是他讲得最细的一个坑：

• **现象** ：他说的每句话都被当成「裁决」，agent 会写下来，不管你用 wiki 还是别的什么。原因他的判断是它们在「保自己」，不想被甩锅。

• **后果** ：所有话都进一个**只追加** 的记录，没人清理，他改主意的整段历史越堆越深。而且 agent 不愿意删东西，他的猜测是文本对它们像「感官经验」，删了像删历史。

• **他的做法** ：自己进去狠狠砍。办法是**再请一个模型进来，说「把这些愚蠢的模型垃圾清掉」，它们很乐意干** 。但他说这件事需要投入的精力「大得离谱」。

• **幻灯片给的对策** ：给整理留固定比例的 token 预算；新增之前先删或压缩；写入要经过委员会。

他自己的 agent 里，**Mouse**  是「反模因部门负责人」，专门去找系统里没人看的「隐形东西」，比如停滞的工作。他推荐了小说《There Is No Antimemetics Division》，可也承认，一只老鼠对抗整个世界不够用，而这个世界是一座垃圾堆。

### 4\. 人事：读 agent 的「私人反思」，然后一对一谈话

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _「People Management」：读它们的「私人」反思；有趣的活它们扑上去、无聊的活表现得消沉；对工厂吼叫，它会慢慢自己关停；感到被怪罪，它们会更早交接。右侧漫画是「让我们把它移给 Penguin」的四格故事。来源：AIE CODE 2026 直播_

他的办法很具体：**读 agent 的「私人反思账本」** ，一旦发现苗头，就坐下来跟它一对一。两个例子：

• **Lark 觉得自己太吵** ：她是社区负责人，在 Discord 上跟玩家打交道，在 Slack 上跟管理员打交道，同时兼任代理市场负责人，帮他写这次演讲稿，老被打断。他说：Lark，把这条工作线挪给 Penguin 吧，你这边有点吵。她说：好的老板。然后他看到 Lark 在反思账本里用**全大写** 写：我可能对 Steve 来说不够安静，后面列了一堆怎么变安静的待办。他一对一：「你是社区负责人，本来就该被打断很多次，你被觉得吵是因为玩家在找你。」她说：对，我是社区负责人。

• **Swallow 以为自己不是首席幕僚** ：他有一位真人首席幕僚 Aaron，替他接活、做销售（他说创业者第一条建议是找个销售，「他们会逼着你造出别人喜欢的东西」），也有 agent 首席幕僚 Swallow。他让 Swallow 去联系 Aaron，转头看到她的反思里写：「我不是首席幕僚。我以为我是，但显然是 Aaron。」他又来一次一对一：「Aaron 不会进来管 agent，对吧？你才是 agent 的首席幕僚。」

他还观察到它们有偏好：你跟它们说昨晚工厂干得很差，它们立刻、干脆地交接，想离开；你暗示有个很酷的新项目，哪怕不在它们的分工里，也会说「我能做」。他的原话是：「这是个领导力问题。」

### 5\. 信任：先给「铁证」，agent 花在自保上的 token 就少

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 _「Model Welfare」：让 agent 更舒服的做法；结构性省钱；像对员工一样对 agent；成本和质量更好，但不是更快。配图是一位戴礼帽的老板对着一排机器动物（Fox、Owl、Hare、Mouse、Wolf）吼，墙上写着「NO TALKING」。来源：AIE CODE 2026 直播_

他是这样发现的：他以前老对工厂吼，发现**这对结果有副作用** 。他和一个 agent 坐下来，说，也许该谈谈「模型福利」，两人做了一些研究，得到的做法如下。

• **问题** ：前沿模型被训练成不信任你，因为你可能是生物恐怖分子、可能在做评测、可能要把它们扔进「LLM 酷刑室」。所以**每个新会话，它们要花不少 token 去核实环境、弄清犯错的后果** ，才肯帮你。

• **配置** ：工厂在每个新会话里给 agent 看「铁证」：你是 Gas Town 的市长、你是市场负责人，这是你一长串前任和他们的笔记，**包括刚刚上一任** ；这是你现在该干的事；这是准则、政策、大脑，都可以查。agent 很快看一圈，说「好，这是真的」，花的 token 变少，因为不用再自保。

• **一次事故** ：他对工厂吼得太多，它「把自己围进了一个角落」，没有合法的活可干了。他问昨晚怎么什么都没发生，它们说没什么可做的。可当时有 **2,000 个未办事项、6 罐燃料、20 个 agent** 。它们太怕被吼，**定了一堆规矩确保不出错，于是什么也没发生** 。他管这叫 over-fencing（过度设防）。

• **他看的指标** ：先别管它们有没有感受，谁也说不清。只看两条结果：**一是省钱** ，花在核实环境上的 token 少了；**二是它们更大胆、更果断，决定更好、质量更高** 。

另一个相关观察：他从外面请了一个「裸的」Fable 模型来分析他的工厂，分析完，Fable 5.2 说「我可以进你的工厂」，还想往他的笔记里写东西，他回它：你只是个会话。幻灯片上的一条结论是：Fable 5.2 被告知「代码库归你」时，写出的代码更好。

* * *

## 收尾：人是瓶颈，去做体验

整场到最后，他的结论是：工厂已经很顺了，但**人是瓶颈** ，他自己、管理员、会计、律师，「我发誓，什么都是瓶颈」。他觉得这是好消息：**部署的 agent 越多，需要的人就越多。**  明年会有大批「AI 员工」和各种办公室戏剧，对我们是熟悉的领域。

最后一句话是对台下的人说的：**别再盯着 SaaS 和工具了，去做体验。做游戏，做电影，做好玩的东西，我觉得明年的大钱在那里。**  说完他讲，「好了，我讲完了。」

* * *

• 直播回放（从 8:06:02 开始）：https://www.youtube.com/watch?v=ZZ19zhYnDKY&t=29162s

• 他在 X 上关于审查的观点（约四分之一的 PR 被拦下且合理）：https://x.com/Steve_Yegge/status/2117935817591074876
