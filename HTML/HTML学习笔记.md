HTML简介：
HTML 不是一门编程语言，而是一种用于定义内容结构的标记语言。HTML 由一系列的元素组成，这些元素可以用来包围不同部分的内容，使其以某种方式呈现或者工作。
这个元素的主要部分有：
开始标签（Opening tag）：包含元素的名称，被大于号、小于号所包围。表示元素从这里开始或者开始起作用——在本例中即段落由此开始。
结束标签（Closing tag）：与开始标签相似，只是其在元素名之前包含了一个斜杠。这表示着元素的结尾——在本例中即段落在此结束。初学者常常会犯忘记包含结束标签的错误，这可能会产生一些奇怪的结果。
内容（Content）：元素的内容
元素（Element）：开始标签、结束标签与内容相结合，便是一个完整的元素，其中也可以包含属性（Attribute）。

HTML基本文档：

<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>page name</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image" />
  </body>
</html>

<!DOCTYPE html>——文档类型。这是必不可少的开头。
<html></html>——<html> 元素。该元素包含整个页面的所有内容，有时候也称作根元素。里面也包含了 lang 属性，写明了页面的主要语种。
<head></head>——<head> 元素。所有那些你加到页面中，且不向用户展示的页面内容，都以这个元素为容器。其中包含诸如提供给搜索引擎的关键字和页面描述、用于设置页面样式的 CSS、字符集声明等等。
<meta charset="utf-8">——该元素指明你的文档使用 UTF-8 字符编码
<meta name="viewport" content="width=device-width">——视口元素可以确保页面以视口宽度进行渲染，避免移动端浏览器上因页面过宽导致缩放。
<title></title>——<title> 元素。该元素设置页面的标题，显示在浏览器标签页上，也作为收藏网页的描述文字。
<body></body>——<body> 元素。该元素包含期望让用户在访问页面时看到的全部内容，包括文本、图像、视频、游戏、可播放的音轨或其他内容。

HTML元素：
1.标题元素<h1>-<h6>:
<h1>主标题</h1>
<h2>顶层标题</h2>
<h3>子标题</h3>
<h4>次子标题</h4>

2.段落元素<P>：
<p>这是一个段落</p>

3.无序列表元素<ul>:
<ul>
  <li>1</li>
  <li>2</li>
  <li>3</li>
</ul>

4.有序列表元素<ol>:
<ol>
  <li>1</li>
  <li>2</li>
  <li>3</li>
</ol>

5.链接元素<a>:
<a href="链接地址" title="补充信息">链接名称</a>

6.字体倾斜元素<em>:
<p><em>倾斜</em></p>

7.字体加粗元素<strong>:
<p>这<strong>加粗</strong></p>

8.列表元素<dl>：
描述列表使用与其他列表类型不同的闭合标签——<dl>；此外，每一项都用 <dt>（description term）元素闭合。每个描述都用 <dd>（description definition）元素闭合。
<dl>
  <dt>1</dt>
  <dd>
  ...
  </dd>
  <dt>2</dt> //可以有多个描述
  <dd>
  ...
  </dd>
  <dd>
  ...
  </dd>
</dl>

9.引用元素<blockquote>：

10.缩略元素<addr>:

11.标记联系方式的元素<address>:

12.上标和下标元素，<sup> 和 <sub> :

13.标记计算机代码的元素:
<code>：用于标记计算机通用代码。
<pre>：用于保留空白字符（通常用于代码块）——如果文本中使用了缩进或多余的空白，浏览器将忽略它，你将不会在呈现的页面上看到它。但是，如果你将文本包含在 <pre></pre> 标签中，那么空白将会以与你在文本编辑器中看到的相同的方式渲染出来。
<var>：用于标记具体变量名。
<kbd>：用于标记输入电脑的键盘（或其他类型）输入。
<samp>：用于标记计算机程序的输出。

14.将时间和日期标记为可供机器识别的格式的 <time> 元素:
<time datetime="204-01-01">2024 年 1 月 1 日</time>

15.语义化标记，明确区段的专用标签：
<header>：页眉。
<nav>：导航栏。
<main>：主内容。主内容中还可以有各种子内容区段，可用<article>、<section> 和 <div> 等元素表示。
<aside>：侧边栏，经常嵌套在 <main> 中。
<footer>：页脚。

16.换行元素<br>：

17：水平分割线<hr>：

18.<figure> 和 <figcaption>元素：
为图片提供一个语义容器，在标题和图片之间建立清晰的关联

19.图像元素<img>:
<img src="图片路径" alt="描述文本" />

20.视频元素<viddeo>:
<video src="视频路径" controls>
  <p>
    你的浏览器不支持 HTML5 视频。可点击<a href="链接地址">此链接</a>观看
  </p>
</video>
使用 controls 来包含浏览器提供的控件界面
<video> 标签内的内容这个叫做后备内容 — 当浏览器不支持 <video> 标签的时候，就会显示这段内容，这使得我们能够对旧的浏览器提供回退内容。
<video controls>
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>
    你的浏览器不支持 HTML5 视频。可点击<a href="rabbit320.mp4">此链接</a>观看
  </p>
</video>
现在我们将 src 属性从 <video> 标签中移除，转而将它放在几个单独的标签 <source> 当中。在这个例子当中，浏览器将会检查 <source> 标签，并且播放第一个与其自身 codec 相匹配的媒体。每个 <source> 标签页含有一个 type 属性，这个属性是可选的，但是建议你添加上这个属性 — 它包含了视频文件的 MIME types ，同时浏览器也会通过检查这个属性来迅速的跳过那些不支持的格式。如果你没有添加 type 属性，浏览器会尝试加载每一个文件，直到找到一个能正确播放的格式，这样会消耗掉大量的时间和资源。
<video
  controls
  width="400"
  height="400"
  autoplay
  loop
  muted
  poster="poster.png">
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>
    你的浏览器不支持 HTML5 视频。可点击<a href="rabbit320.mp4">此链接</a>观看
  </p>
</video>
新的特性：
width 和 height
你可以用属性控制视频的尺寸，也可以用 CSS 来控制视频尺寸。无论使用哪种方式，视频都会保持它原始的长宽比 — 也叫做纵横比。如果你设置的尺寸没有保持视频原始长宽比，那么视频边框将会拉伸，而未被视频内容填充的部分，将会显示默认的背景颜色。
autoplay
这个属性会使音频和视频内容立即播放，即使页面的其他部分还没有加载完全。建议不要应用这个属性在你的网站上，因为用户们会比较反感自动播放的媒体文件。
loop
这个属性可以让音频或者视频文件循环播放。同样不建议使用，除非有必要。
muted
这个属性会导致媒体播放时，默认关闭声音。
poster
这个属性指向了一个图像的 URL，这个图像会在视频播放前显示。通常用于粗略的预览或者广告。
preload
这个属性被用来缓冲较大的文件，有 3 个值可选：
"none" ：不缓冲
"auto" ：页面加载后缓存媒体文件
"metadata" ：仅缓冲文件的元数据
21.音频元素<audio>:
<audio> 标签与 <video> 标签的使用方式几乎完全相同
<audio> 标签不支持 width/height 属性 — 由于其并没有视觉部件，也就没有可以设置 width/height 的内容。同时也不支持 poster 属性.除此之外，<audio> 标签支持所有 <video> 标签拥有的特性

页面添加网页图标的方式有：
1。将其保存在与网站的索引页面相同的目录中，以 .ico 格式保存（大多数浏览器支持更通用的格式，如 .gif 或 .png）
2.将以下行添加到 HTML 的 <head> 块中以引用它：
<link rel="icon" href="favicon.ico" type="image/x-icon" />

在 HTML 中应用 CSS 和 JavaScript：
<link rel="stylesheet" href="my-css-file.css" />
<script src="my-js-file.js" defer></script>
（同时最好加上 defer 以告诉浏览器在解析完成 HTML 后再加载 JavaScript。这样可以确保在加载脚本之前浏览器已经解析了所有的 HTML 内容。这样你就不会因为 JavaScript 试图访问页面上不存在的 HTML 元素而产生错误）
