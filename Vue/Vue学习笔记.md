安装与创建项目：
NPM安装：
在用 Vue.js 构建大型应用时推荐使用 cnpm 安装，cnpm 能很好地和 Webpack 或 Browserify 模块打包器配合使用，然后在命令行中运行以下命令：
# 最新稳定版
$ npm init vue@latest
这一指令将会安装并执行 create-vue，它是 Vue 官方的项目脚手架工具。

$ npm init vue@latest
Need to install the following packages:
  create-vue@3.6.1
Ok to proceed? (y) y

Vue.js - The Progressive JavaScript Framework
# 这里需要进行一些配置，项目名输入 runoob-vue3-test，其他默认回车即可
&#x2714; Project name: … runoob-vue3-test
&#x2714; Add TypeScript? … No / Yes
&#x2714; Add JSX Support? … No / Yes
&#x2714; Add Vue Router for Single Page Application development? … No / Yes
&#x2714; Add Pinia for state management? … No / Yes
&#x2714; Add Vitest for Unit Testing? … No / Yes
&#x2714; Add an End-to-End Testing Solution? › No
&#x2714; Add ESLint for code quality? … No / Yes

Scaffolding project in /Users/tianqixin/runoob-test/runoob-vue3/runoob-vue3-test...

Done. Now run:

  cd runoob-vue3-test
  npm install
  npm run dev
在项目被创建后，通过以下步骤安装依赖并启动开发服务器：

$ cd runoob-vue3-test
$ npm install
$ npm run dev
  VITE v4.3.4  ready in 543 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h to show help

我们可以通过 vue ui 命令来打开图形化界面创建和管理项目
$ vue ui
&#x1f680;  Starting GUI...
&#x1f320;  Ready on http://localhost:8000
...


pnpm：
pnpm create vue@latest

vite:
npm init vite-app <project-name>或者pnpm create vite-app <project-name>

打包：
npm run build
执行完成后，会在 Vue 项目下会生成一个 dist 目录，该目录一般包含 index.html 文件及 static 目录，static 目录包含了静态文件 js、css 以及图片目录 images（如果有图片的话）。

目录结构：
vue-cli:
![alt text](https://www.runoob.com/wp-content/uploads/2021/02/7C26D06C-4B1B-4E80-BBE1-E407C3E945B3.jpg)
vite:
![alt text](https://www.runoob.com/wp-content/uploads/2021/02/7C797674-06CF-4E87-B344-63990EF519B6.jpg)
目录解析：
build	        项目构建(webpack)相关代码
config	        配置目录，包括端口号等。我们初学可以使用默认的。
node_modules	npm 加载的项目依赖模块
src	            
这里是我们要开发的目录，基本上要做的事情都在这个目录里。里面包含了几个目录及文件：
assets:     放置一些图片，如logo等。
components: 目录里面放了一个组件文件，可以不用。
App.vue:    项目入口文件，我们也可以直接将组件写这里，而不使用 components 目录。
main.js:    项目的核心文件。
index.css:  样式文件。
static	    静态资源目录，如图片、字体等。
public	    公共资源目录。
test	    初始测试目录，可删除
.xxxx文件	 这些是一些配置文件，包括语法配置，git配置等。
index.html	首页入口文件，你可以添加一些 meta 信息或统计代码啥的。
package.json	项目配置文件。
README.md	项目的说明文档，markdown 格式
dist	    使用 npm run build 命令打包后会生成该目录。

函数：
const app = Vue.createApp({ /* 选项 */ })
传递给 createApp 的选项用于配置根组件。在使用 mount() 挂载应用时，该组件被用作渲染的起点。
一个简单的实例：
Vue.createApp(HelloVueApp).mount('#hello-vue')
方法：
我们可以在组件中添加方法，使用 methods 选项，该选项包含了所需方法的对象

vue指令：
它们可以在 HTML 模板中以 v- 开头的特殊属性形式使用，用于将响应式数据绑定到 DOM 元素上或在 DOM 元素上进行一些操作。
v-bind	用于将 Vue 实例的数据绑定到 HTML 元素的属性上。
v-if	用于根据表达式的值来条件性地渲染元素或组件。
v-show	v-show 是 Vue.js 提供的一种指令，用于根据表达式的值来条件性地显示或隐藏元素。
v-for	用于根据数组或对象的属性值来循环渲染元素或组件。
v-on	用于在 HTML 元素上绑定事件监听器，使其能够触发 Vue 实例中的方法或函数。
v-model	用于在表单控件和 Vue 实例的数据之间创建双向数据绑定。


