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
1.通过style属性操作CSS
对象.style。样式属性 = 值
2.操作类名（className）操作CSS
元素。className = 'active'
好处：修改多个样式
tips：直接使用会覆盖以前的类名
3.通过classList操作类控制CSS
元素.classList.add('类名')
元素.classList.remove('类名')
元素.classList。toggle('类名')
className和classList的区别：
修改大量样式的更方便
修改多样式的时候方便
classList是追加和删除不影响以前类名
