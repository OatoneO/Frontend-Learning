DOM:
根据CSS选择器来获取DOM元素：
document.querySelector('CSS选择器')
参数：包含一个或多个有效的CSS选择器字符串
返回值：CSS选择器匹配的NodeList对象集合
document。querySelectorAll('CSS选择器')
区别：一个获取第一个，一个获取全部（但得到的是伪数组）

操作元素内容：
对象.innerText属性:
将文本内容添加/更新到任意标签位置；显示纯文本，不解析标签
对象.innerHTML属性：
将文本内容添加/更新到任意标签位置；会解析标签，多标签建议使用模版字符

操作元素样式属性：
1.通过style属性操作CSS：
对象.style。样式属性 = 值
2.操作类名（className）操作CSS：
元素.className = 'active'
好处：修改多个样式
tips：直接使用会覆盖以前的类名
3.通过classList操作类控制CSS：
元素.classList.add('类名')
元素.classList.remove('类名')
元素.classList。toggle('类名')
className和classList的区别：
修改大量样式的更方便
修改多样式的时候方便
classList是追加和删除不影响以前类名

操作表单元素属性：
1.获取：
DOM对象.属性名
2.设置：
DOM对象.属性名 = 新值

自定义属性：
data-开头

间歇函数：
开启定时器
setInterval(函数名(不加括号)，间隔时间（毫秒）)
setInterval('函数名（）'，间隔时间)
关闭定时器：
let 变量名 = setInterval(函数名，间隔时间)
clearInterval(变量名)

事件监听：
元素对象.addEventListener('事件类型', 要执行的函数)
三要素：
事件源：某个dom元素被事件触发了，要获取dom元素
事件类型：如鼠标单击click，鼠标经过mouseover等
事件调用的函数：要干什么事情

事件类型有：
1.鼠标事件：click 鼠标点击；mouseenter 鼠标经过；mouseleave 鼠标离开
2.焦点事件：focus 获得焦点；blur 失去焦点
3.键盘事件：keydown 键盘按下触发；keyup 键盘抬起触发
4.文本事件：input 用户输入事件

事件对象：
获取事件对象：
在事件绑定的回调函数的第一个参数就是事件对象
部分常用属性：
type：获取当前的事件类型
clientX/clientY：获取光标相对于浏览器可见窗口左上角的位置
offsetX/offsetY：获取光标相对于当前DOM元素左上角的位置
key：用户按下的键盘的值

环境对象：
函数内部特殊的变量this，它代表当前函数运行时所处的环境
作用：弄清楚函数对象，可以让代码更简洁
规则：谁调用，this指向谁

回调函数：
如果将函数A作为参数传递给函数B时，函数A为回调函数
