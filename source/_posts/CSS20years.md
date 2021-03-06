---
title: 译文：20 年 CSS 历史
tags:
  - CSS
category:
  - 译文
date: 2018-12-11 17:28:27
---


> 原文：[A brief history of CSS until 2016](https://www.w3.org/Style/CSS20/history.html)

## 速读版本

[20 Years of CSS](https://www.w3.org/Style/CSS20/)

接下来的是详细的历史版本

## CSS 的冒险

CSS 的冒险从 1994 年开始。在 CERN 工作的 Håkon Wium Lie，CERN 网络的摇篮，在这里网络最开始被用作电子出版的平台。然而，缺少发布平台的一个关键部分：无法设置文档样式。例如，无法在网页中描述类似报纸的布局。在麻省理工学院媒体实验室从事个性化的报纸演示后，Håkon 认为需要一种用于网络的样式表语言。

浏览器中的样式表并不是一个全新的想法。从1990年开始，文档结构与文档布局的分离一直是HTML的目标。Tim Berners-Lee以这样的方式编写了他的NeXT浏览器/编辑器，他可以通过简单的样式表来确定样式。但是，他考虑到每个浏览器决定如何最好地向其用户显示页面的问题，所以并没有发布样式表的语法。1992年，Pei Wei 开发了一款名为 Viola 的浏览器，这款浏览器有自己的样式表语言。

但是，随后的浏览器为用户提供的影响样式的选项越来越少。1993年，NCSA Mosaic 成为网络流行的浏览器。然而，Stylewise 是一个进度很落后，它只允许其用户更改某些颜色和字体。

与此同时，网页编写者抱怨他们没有足够多的选项来控制样式。Web 作者的第一个问题之一就是如何更改元素的字体和颜色。那时，HTML没有提供这种功能 - 这是理所当然的。 1994 年早些时候发送到 www-talk 邮件列表的消息的摘录让人感觉到作者和实现者之间的紧张关系：

> 事实上，在过去的一年里，我不断地告诉成群结队的人（字面意思），这是一个令人高兴的喜悦之源。它来了 - 在TeX，Microsoft Word以及其他所有常见的文本处理环境中以微不足道的方式控制文档的外观：“抱歉，你搞砸了。”

发布这条消息的作者是 Marc Andreessen，他是 NCSA Mosaic 背后的程序员之一。他后来成为Netscape的联合创始人，Netscape是一家渴望满足作者要求的公司。1994年10月13日，Marc Andreessen向www-talk宣布，Mozilla的第一个beta版本（后来转变为Netscape Navigator）可用于测试。在新标签中，新浏览器支持的是中心，很快就会有更多标签。

在Netscape宣布推出新浏览器的前三天 1994 年 10 月 9 日，Håkon 发布了级联HTML样式表提案的初稿。在幕后，Dave Raggett（HTML 3.0的主要架构师）鼓励在即将到来的芝加哥Mosaic和Web会议之前发布草稿。戴夫已经意识到HTML将永远不会变成页面描述语言，并且需要一个更专用的机制来满足作者的要求。虽然该文件的第一版尚不成熟，但它为讨论提供了有用的基础。

回应CSS第一稿的人中有Bert Bos。那时，他正在构建Argo，这是一款带有样式表的高度可定制的浏览器，他决定与Håkon合作。这两个提案都与现今的CSS有所不同，但不难理解原始概念。Argo风格语言的一个特点是，除了HTML之外，它还可以应用于其他标记语言。这也成为CSS中的设计目标，HTML很快就从规范的标题中删除了。 Argo还有其他高级功能，但没有进入CSS1，特别是属性选择器和生成的文本。这两个功能都必须等待CSS2。

「层叠样式表」不是当时唯一提出的样式语言。 来自Viola浏览器的Pei Wei语言，大约10个其他样式表语言提案被发送到www-talk和www-html邮件列表。 然后，有一个DSSSL，一种复杂的样式和转换语言正在ISO开发用于打印SGML文档。 可以想象，DSSSL也可以应用于HTML。 但是，CSS有一个功能可以区别于其他功能：它考虑到在网络上，文档的风格不能由作者或读者自己设计，但他们的愿望必须 以某种方式组合或级联; 事实上，不仅是读者和作者的愿望，还有显示设备和浏览器的功能。

按照计划，1994年11月在芝加哥举行的网络会议上提出了最初的CSS提案。开发者日的演讲引起了很多讨论。 首先，作者和用户偏好之间的平衡概念是新颖的。 一个虚构的屏幕截图显示了一个滑块，一边是标签用户，另一边是作者。 通过调整滑块，用户可以改变他自己的喜好和作者的喜好。 其次，一些人认为CSS对于它的设计任务太简单了。 他们认为，要对文档进行样式化，需要使用完整的编程语言。 CSS是一个简单的声明性格式，它完全相反的方向。

在政治斗争之外，技术工作仍在继续。 www风格的邮件列表创建于1995年5月，其中的讨论经常影响CSS规范的开发。 大约10年后，邮件列表的档案中有超过16,000封邮件。 预计20年后会超过8万！

![(photo) sitting at a dinner table](https://www.w3.org/Style/CSS20/950636c-W3C.jpg)

<center>Håkon Wium Lie, 12 December 1995</center>

1995年，万维网联盟（W3C）开始运作，很多公司加入了联盟，该组织成立。开展各种主题的研讨会是W3C成员和工作人员会面和讨论未来技术发展的成功方式。因此决定组织一次以样式表为主题的研讨会，工作在样式表上的W3C技术人员（即Håkon和Bert）现在位于法国南部的索菲亚 - 安提波利斯，W3C在那里建立了欧洲站点。法国南部并不是吸引研讨会参与者的最佳地点，但由于许多潜在的参与者都在美国，因此决定在巴黎举办研讨会，国际航班更好。研讨会也是一个实验，看看W3C是否有可能在美国境外组织活动。事实上，这是可能的，而研讨会是确保样式表在网络上合法地位的里程碑。参与者包括微软的Thomas Reardon，他承诺在即将推出的Internet Explorer版本中支持CSS。

![(photo) sitting at a dinner table](https://www.w3.org/Style/CSS20/950628c-W3C.jpg)

<center>Bert Bos, 12 December 1995</center>

1995年底，W3C成立了HTML编辑评审委员会（HTML ERB），以批准未来的HTML规范。 由于样式表属于新组成员感兴趣的范围，因此CSS规范被视为工作项，目标是将其作为W3C建议书。 HTML ERB的成员之一是Netscape的Lou Montulli。 微软表示它正在浏览器中添加CSS支持后，让Netscape加入也很重要。 否则，我们可以通过支持不同规范的浏览器看到Web在不同方向上的分歧。 HTML ERB中的战斗是漫长而艰难的，但CSS级别1终于在1996年12月成为W3C推荐标准。

1997年2月，CSS在W3C内部建立了自己的工作组，新组开始研究CSS1没有解决的功能。 该小组由来自曼彻斯特大学招募到W3C的苏格兰人Chris Lilley担任主席。 CSS级别2于1998年5月成为推荐标准。从那时起，该小组就新的CSS模块和CSS 2的勘误表并行工作。

W3C工作组有成员（1999年约15个，2016年约115个），由 作为W3C成员的公司和组织。 他们来自世界各地，所以会议通常通过电话，每周约一个小时。 每年大约四次，他们在世界的某个地方相遇。

## 浏览器

没有关于浏览器的部分，CSS传奇是不完整的。 如果没有浏览器，CSS将仍然是一个只有学术兴趣的崇高建议。 支持CSS的第一个商业浏览器是微软的Internet Explorer 3，它于1996年8月发布。那时，CSS1规范尚未成为W3C推荐标准，HTML ERB中的讨论导致微软开发人员的变化，导致 克里斯威尔逊无法预见。 IE3可靠地支持大多数颜色，背景，字体和文本属性，但它没有实现太多的盒子模型。

宣布支持CSS的下一个浏览器是Netscape Navigator 4.0版。 自成立以来，Netscape一直对样式表持怀疑态度，该公司的首次实施结果证明是一种半心半意的企图阻止微软声称自己比Netscape更符合标准。 Netscape实现支持广泛的功能 - 例如，浮动元素 - 但Netscape开发人员没有时间完全测试所有支持的功能。 Navigator 4.0 中无法使用许多CSS属性。

Netscape通过将CSS规则转换为JavaScript片段在内部实现了CSS，然后与其他脚本一起运行。 该公司还决定让开发人员编写JSSS，从而完全绕过CSS。 如果JSSS成功了，那么Web将会有一个不必要的样式表。 对于CSS而言，幸运的是，结果并非如此。

与此同时，微软继续努力将Netscape从卫冕的浏览器中取代。 在Internet Explorer 4中，浏览器显示引擎（其中包括负责渲染CSS）被代号为Trident的模块所取代。 Trident删除了IE3中的许多限制，但也带来了一系列限制和错误。 微软受到Web标准项目（WaSP）的压力，该项目于1998年11月发布了IE的十大CSS问题（参见图1）。

![[image]](https://www.w3.org/Style/CSS20/history-wasp.png)

<center>图1. WaSP项目跟踪浏览器与W3C建议书的一致性。 他们的第一个评论之一是Microsoft Internet Explorer中的CSS支持。</center>

后续版本的Internet Explorer大大提高了对CSS的支持。

<div style="float:left; margin-right: 20px;"><img alt="Photo: a cellphone with a Web page on its screen." src="https://www.w3.org/Style/CSS20/history-opera-ssr.png"><small><br >图2. Opera的小屏幕<br>渲染将页面转换为列。</small>
</div>
<p>
  冒险进入CSS的第三个浏览器是Opera。 这家来自挪威小公司的浏览器在1998年成为头条新闻，因为它很小（适合放在软盘上！）并可定制，同时支持微软和Netscape提供的大型产品中的大部分功能。 Opera 3.5于1998年11月发布，支持CSS1的大部分内容。 Opera开发人员（即GeirIvarsøy）也有时间在发货前测试CSS实现，这在这项业务中是一个新鲜事物。 Håkon对Opera的技术印象深刻，于1999年加入公司担任首席技术官。Opera浏览器的一个重要市场是手机。 通过重新格式化页面以适应小屏幕（@media在这里很方便），Web已从桌面中释放（参见图2）。
</p><p>
  Netscape的人们通过当时的新颖举措回应了日益激烈的竞争：他们开源了浏览器的源代码。 随着源代码的公开，任何人都可以检查其产品的内部，改进它，并基于进行竞争的浏览器。许多代码，包括CSS实现，在发布后不久终止，并且Mozilla项目形成为 构建新一代浏览器。 CSS处于重要的规范中，志愿者花费了无数小时来确保根据规范显示页面。 一些浏览器基于Mozilla代码，包括Galeon和Firefox。
</p><p>
  Apple经常被视为技术先驱，但长期以来，它并没有在Web浏览器上花费太多资源。 Apple将其留给微软为其机器构建浏览器，而Mac的Internet Explorer实际上比Windows版本的浏览器更好地支持CSS。 2003年，微软停止了对Mac的支持，Apple公布了一款名为Safari的新浏览器。 Safari并不是全新的 - 它基于开源的Konqueror浏览器，该浏览器是为在Linux上运行的KDE系统开发的。
</p><p>
  对于Web设计人员来说，拥有基于Web标准的多种竞争产品是个好消息。 虽然有必要尝试测试您的页面在所有浏览器中都能很好地显示，但是网页可以在各种机器上显示这一事实是一个巨大的改进：
</p><p>
  任何拍打这个页面的人最好用网页上的浏览器X标签查看，这对于过去的糟糕时光，在Web之前，当你几乎没有机会阅读另一台计算机，另一个文字处理器， 或另一个网络。<cite>– Tim Berners-Lee in Technology Review, July 1996</cite>
</p>

## 超越浏览器

CSS传奇不只是关于Web浏览器。 在过去几年中，为Web浏览器编程的少数人之外的许多人都对CSS做出了重要贡献。

CSS1测试套件是CSS和W3C的标志性开发。 当前两个CSS实现出来并且可以进行比较时，我们意识到存在问题。 您不能指望仅在一个浏览器中测试的样式表才能在另一个浏览器中工作。 为了纠正这种情况，Eric Meyer  - 在无数其他志愿者的帮助下 - 开发了一个测试套件，实施者可以测试，同时还有时间来解决问题。 Todd Fahrner于1998年10月创建了酸测试，这成为了最终的挑战。 见图3。

![[Several colored boxes next and above each other]](https://www.w3.org/Style/CSS20/sec5526c.gif)

<center>图3.酸测试。</center>

当测试套件可用时，有人必须进行测试。 Brian Wilson在测试CSS实现并在Web上提供结果方面做得非常出色。

我们还应该提到最近几年GérardTalbot和Geoffrey Sneddon在官方CSS testuite上的工作。 当然还有Peter Linss，他的Shepherd服务器在查看测试存在，运行它们以及生成结果报告方面提供了很大的帮助。

如果没有引人注目的内容，CSS就没有达到目的。 Dave Shea创建了[CSS Zen花园](http://www.csszengarden.com/)，向同行图形艺术家展示为什么要认真对待CSS。 他和许多创建提交内容的人一起向人们展示了如何创造性地使用CSS。

Web已被困在桌面上太久了。 在手机上提供它是一个重要的逃脱。 Michael Day和刘学红向我们展示了另一条出路：Prince格式化程序将HTML和XML文档转换为PDF，完全基于CSS。 该产品使Håkon和Bert放弃了传统的文字处理器并使用Web标准。 [他们的书](https://www.w3.org/Style/LieBos3e/)完全是用HTML和CSS编写的。

## 网页字体

CSS2包含一个名为Web Fonts的功能，即能够在Web文档中嵌入字体。 想法是，想要特定字体的设计师实际上可以提供字体以及样式表。 在十年期间，只有Microsoft的Internet Explorer浏览器实现了该功能。 （Netscape在短期内实现了一种替代方案，它没有使用CSS，效果不佳，在很多国家可能都是非法的，因为它略微改变了每种字体的外观。）

Web Fonts没有实现的原因是双重的。 首先，很少有字体允许分发版权。 大多数字体可用于在本地打印文档，但不允许将它们放在Web上。

其次，Microsoft和Monotype开发了一种称为EOT（嵌入式OpenType）的格式，它在字体中包含可以用它们呈现的文档的名称（URL）。 这允许EOT字体在Web上与文档一起提供，因为它现在不能用于任何其他文档。 但是，这种格式是专有的，除了微软之外别无其他人可以使用它。

所有这些都在2008年初发生了变化。到那时，还有更多免费字体，即设计师允许它们在网上免费分发的字体。 因此，Håkon开始游说浏览器制造商最终实施Web Fonts（用于标准TrueType和OpenType格式的字体），Bert询问Microsoft是否无法打开EOT，以便其他人也可以实现它。 5月，Microsoft和Monotype根据免版税许可向W3C[提交了EOT](https://www.w3.org/Submission/2008/01/Comment)。 浏览器开始实现对下载TrueType和OpenType字体的支持。

然而，在进一步讨论之后，大多数浏览器制造商决定不实施EOT，而是要求W3C开发新的字体格式。 原因是他们更喜欢使用gzip压缩算法（已经用于HTTP），而不是为EOT使用的MicroType Express算法添加新代码。

这种新格式成为[WOFF](https://www.w3.org/TR/WOFF/)。 它不是将文档的URL嵌入字体中，而是依赖于HTTP功能（原始标题），它允许提供文档URL的域部分：不如完整URL精确，但对大多数字体仍然足够好制造商。

然而，最后，WOFF仍然采用了EOT的MicroType Express算法和新的压缩算法（Brotli）的一部分，因为它允许比gzip更好的压缩。

网络字体变得非常流行。 免费字体直接以TrueType或OpenType格式使用。 较少的免费字体使用WOFF和EOT格式。

现在有在线服务，您可以在其中找到和下载字体（免费和非免费）。 有些人甚至提出在他们的服务器上托管字体。 在某些情况下甚至是免费的。 （这意味着它们提供带宽，但作为回报，它们收集字体使用情况的统计数据）。

## 新方向：书籍和图形用户界面

CSS的开发并没有停止。 CSS现在有60多个模块定义了不同的功能，有些已经成为标准的一部分，有些还在开发中。

现在通常用CSS制作书籍。然而，并非所有书籍都是因为CSS仍然缺少更复杂布局的功能。这是语言扩展的一个方向。

电子书也使用CSS，这需要其他功能。 EPUB是电子书最广泛实施的格式。 它由IDPF开发。 IDPF和W3C目前（2016年12月）正在合并其业务。 然后应该在W3C制作下一个EPUB版本，并且更容易开发书籍和电子书的CSS功能。

使用由HTML和CSS构成的图形用户界面的程序（app）的开发也对CSS提出了新的要求。 一些最新的CSS模块处理用户界面的布局而不是文档。 虽然：因为它们是同一个CSS的一部分，所以如果文档的一部分恰好具有允许它的标记结构，则不会禁止它们用于文档。

随着时间的推移，一些浏览器和其他实现已经消失，并且已经创建了新的实现。 现在还有来自CSS的语言用于除样式文档之外的其他目的。 使用CSS语法（但不是级联和继承模型）的第一种语言可能是由Daniel Glazman撰写的[STTS](http://disruptive-innovations.com/products/stts.html)。 那是在1998年。从那时起，其他人就出现了。 目前使用的三个是[Qt样式表](http://doc.qt.io/Qt-5/stylesheet-syntax.html)，用于在Qt GUI工具包中设置样式小部件，[JavaFX样式表](https://docs.oracle.com/javafx/2/css_tutorial/jfxpub-css_tutorial.htm)，它对Java的JavaFX UI小部件执行相同的操作，以及用于描述地图样式的[MapCSS](http://wiki.openstreetmap.org/wiki/MapCSS)。

很难计算CSS的使用范围，但不使用CSS的HTML页面数量可能不会超过百分之几。 许多人以CSS设计师或CSS引用为生。 关于CSS的书籍数量已无法计算在内。

有一天CSS将被其他东西取代。 但在此之前，CSS将有时间庆祝其21岁生日......

<cite>2016年12月17日，Bert Bos</cite>

## 其他阅读

[20 Years of CSS](https://www.w3.org/Style/CSS20/)