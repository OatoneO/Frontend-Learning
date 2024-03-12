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
