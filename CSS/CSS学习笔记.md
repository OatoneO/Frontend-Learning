css选择器：
所有 HTML 元素的选择：
h1 {
}
class 的选择器：
.box {
}
 id 选择器：
 #unique {
}

伪类和伪元素：
:first-child伪类选择器——这将一直选中文章中的第一个子元素
:hover伪类会在鼠标指针悬浮到一个元素上的时候选择这个元素：
a:hover {
}
::first-line是会选择一个元素（下面的情况中是<p>）中的第一行，类似<span>包在了第一个被格式化的行外面，然后选择这个<span>：
p::first-line {
}

运算符：
选择器可以将其他选择器组合起来，更复杂的选择元素。下面的示例用运算符（>）选择了<article>元素的初代子元素：
article > p {
}

全局选择器：
由一个星号（*）代指的，它选中了文档中的所有内容（或者是父元素中的所有内容，比如，它紧随在其他元素以及邻代运算符之后的时候）：
* {
  margin: 0;
}

css的层叠，优先级与继承：
样式表层叠——简单的说，就是 CSS 规则的顺序很重要；当应用两条同级别的规则到一个元素的时候，写在后面的就是实际使用的规则。
浏览器是根据优先级来决定当多个规则有不同选择器对应相同的元素的时候需要使用哪个规则。
一些设置在父元素上的 CSS 属性是可以被子元素继承的，有些则不能。

控制继承：
CSS 为控制继承提供了五个特殊的通用属性值。每个 CSS 属性都接收这些值。

inherit
设置该属性会使子元素属性和父元素相同。实际上，就是“开启继承”。

initial
将应用于选定元素的属性值设置为该属性的初始值。

revert
将应用于选定元素的属性值重置为浏览器的默认样式，而不是应用于该属性的默认值。在许多情况下，此值的作用类似于 unset。

revert-layer
将应用于选定元素的属性值重置为在上一个层叠层中建立的值。

unset
将属性重置为自然值，也就是如果属性是自然继承那么就是 inherit，否则和 initial 一样

理解层叠：
有三个因素需要考虑，根据重要性排序如下，后面的更重要：
1.资源顺序：资源顺序仅在规则的优先级相同时才体现出来
2.优先级：ID > 类 > 元素；内联样式，即 style 属性内的样式声明，优先于所有普通的样式，无论其优先级如何。
3.重要程度：有一个特殊的 CSS 可以用来覆盖所有上面所有优先级计算，不过需要很小心的使用——!important。用于修改特定属性的值，能够覆盖普通规则的层叠。覆盖 !important 唯一的办法就是另一个 !important 具有相同优先级而且顺序靠后，或者更高优先级。

盒模型：
一般分为区块盒子（block boxes）和行内盒子（inline boxes）。类型指的是盒子在页面流中的行为方式以及与页面上其他盒子的关系。盒子有内部显示（inner display type）和外部显示（outer display type）两种类型。一般来说，可以使用 display 属性为显示类型设置各种值，该属性可以有多种值。

外部显示类型：display：block
1.盒子会产生换行。
2.width 和 height 属性可以发挥作用。
3.内边距、外边距和边框会将其他元素从当前盒子周围“推开”。
4.如果未指定 width，方框将沿行向扩展，以填充其容器中的可用空间。在大多数情况下，盒子会变得与其容器一样宽，占据可用空间的 100%。


css布局

常规布局：
取得元素的内容并将其放在一个独立的元素盒子中，然后在其周边加上内边距、边框和外边距——盒子模型。
默认情况下，一个块级元素会填充其父元素所有的行向空间，并沿着其块向伸长以容纳其内容。行级元素的大小就是其本身的大小。你可以为某些 display 属性值默认为 inline 的元素（例如 <img>）设置 width 或 height，但其 display 仍将保持为 inline。如果你想要控制行级元素的 display 属性，请使用 CSS 将其设置为块级元素（例如，使用 display: block; 或 display: inline-block;，后者混合了两者特性）。

弹性盒子：
长久以来，CSS 布局中唯一可靠且跨浏览器兼容的创建工具只有 floats 和 positioning。这两个工具大部分情况下都很好使，但是在某些方面它们具有一定的局限性，让人难以完成任务。以下简单的布局需求是难以或不可能用这样的工具（floats 和 positioning）方便且灵活的实现的：
在父内容里面垂直居中一个块内容。
使容器的所有子项占用等量的可用宽度/高度，而不管有多少宽度/高度可用。
使多列布局中的所有列采用相同的高度，即使它们包含的内容量不同。
弹性盒子使得很多布局任务变得更加容易。
首先，我们需要选择将哪些元素将设置为弹性的盒子。我们需要给这些 flexible 元素的父元素 display 设置为fles-----display:flex;
flex 模型说明:
当元素表现为 flex 框时，它们沿着两个轴来布局：
主轴（main axis）是沿着 flex 元素放置的方向延伸的轴（比如页面上的横向的行、纵向的列）。该轴的开始和结束被称为 main start 和 main end。
交叉轴（cross axis）是垂直于 flex 元素放置方向的轴。该轴的开始和结束被称为 cross start 和 cross end。
设置了 display: flex 的父元素被称之为 flex 容器（flex container）。
在 flex 容器中表现为弹性的盒子的元素被称之为 flex 项（flex item）。
弹性盒子提供了 flex-direction 这样一个属性，它可以指定主轴的方向（弹性盒子子类放置的地方）——它默认值是 row，这使得它们在按你浏览器的默认语言方向排成一排（在英语/中文浏览器中是从左到右）。改变 flex-direction 属性值为 row-reverse——你会看到仍然有多行布局，但是每一行元素排列的方向和原来是相反的了。

Flex 布局中常用的属性及其作用：

弹性容器属性（应用于父元素）：
display: 定义元素的显示类型为 flex，创建一个弹性容器。

flex-direction: 定义弹性容器内子元素的排列方向，可以是 row（水平）、column（垂直）、row-reverse（水平反转）或 column-reverse（垂直反转）。

flex-wrap: 定义弹性容器内子元素是否换行，可以是 nowrap（不换行）、wrap（换行）或 wrap-reverse（反转换行）。

flex-flow：是 flex-direction 和 flex-wrap 的简写属性，用于同时设置弹性容器的主轴方向和换行方式。

justify-content: 定义弹性容器内子元素在主轴上的对齐方式，可以是 flex-start、flex-end、center、space-between、space-around 或 space-evenly。

align-items: 定义弹性容器内子元素在交叉轴上的对齐方式，可以是 flex-start、flex-end、center、baseline 或 stretch。

align-content: 定义多行弹性容器内子元素在交叉轴上的对齐方式，可以是 flex-start、flex-end、center、space-between、space-around 或 stretch。

弹性项目属性（应用于子元素）：

order: 定义弹性项目的排列顺序，值为整数。

flex-grow: 定义弹性项目在剩余空间中的放大比例。

flex-shrink: 定义弹性项目在空间不足时的缩小比例。

flex-basis: 定义弹性项目在分配多余空间之前的基准大小。

flex: 简写属性，用于设置 flex-grow、flex-shrink 和 flex-basis 的值。

align-self: 用于覆盖弹性容器的 align-items 属性，定义单个弹性项目在交叉轴上的对齐方式。