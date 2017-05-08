## 初级内容

### [开发工具](Tools.md)



### css

[多种居中方法](http://www.xingxin.me/posts/590058affd9e613545f2d1f3) (注意兼容性问题)



### js基本语法

[this绑定的意义](https://segmentfault.com/a/1190000007101339)

import 和 require 的异同点



### es5  es6

http://es6.ruanyifeng.com/ 章节列表上方中文的部分
(简介、转码器可以不用看)

重点：
let const
解构
Promise
await 
[yield](http://es6.ruanyifeng.com/#docs/generator#yield--表达式) [处理异步方法使用co库](http://es6.ruanyifeng.com/#docs/generator-async#co-模块) 



### React(View框架)

jsx



备注：

1. 页面、组件在jsx中必须首字母大写。只有浏览器自带组件（如：div、a、img）才使用首字母小写。
2. xxx




### [Flux](Flux.md)

和MVC不同的设计思想



### Redux(Controller框架)

Redux是Flux设计思想的具体实现，需要先了解Flux

Redux封装了Flux各个模块之间对接的方法，只需要分别编写相关模块并绑定Redux。



connect: 绑定Store和View，并且支持对View需要的数据进行筛选

dispatch: 提交Action给Dispatcher

注册reducer: 接收Action，并修改Store



配合 [react-addons-update](https://github.com/facebook/react/blob/master/docs/docs/addons-update.md) 插件更新数据，保证变更state时是创建而不是修改，并且优化创建效率



> 尝试跑通dva的example
> https://github.com/sorrycc/blog/issues/18



### ant.design

蚂蚁金服界面组件库



### [react-router](react-router.md)

被蚂蚁金服封装在内的页面跳转类库



> 根据 ant 的使用方法新建demo工程，需要完成以下功能：
>
> 1. 参考上个example创建新工程
> 2. 新建页面1，实现点击按钮计数器加1、减1、清空功能，需要使用redux实现
> 3. 新建页面2，实现获取测试工程首页源码字符串，并在当前页面中显示源码
> 4. 以上页面的点击按钮和相关界面，使用ant类库提供的样式



### git基本操作 

安装并会使用 GitHub Desktop

add

commit

push

PR (发起分支合并请求)

冲突解决



### js代码调试方法

[常用调试方法](http://www.runoob.com/w3cnote/js-debugging-skills.html) (debugger、浏览器调试模式打断点  等)

[未被捕获的异常自动断点](https://developers.google.cn/web/tools/chrome-devtools/console/track-exceptions?hl=zh-cn)（高级用法：无论是否被捕获都自动断点调试）



### css 

基本样式

block  inline-block 

flex 

float



### [jest](Jest.md)

js单元测试工具



> 对之前创建的工程编写测试脚本，要求：
>
> 1. 为redux方法编写测试用例，覆盖：加1、减1、清空、获取测试工程首页源码。(注：只需要对models中的相关方法进行测试，不需要执行dispatch)
> 2. 用快照接口(toMatchSnapshot)，分别为 增减界面 和 显示源码页 面编写测试用例
>
> 注： 让测试用例支持“imoprt”方法，需要将[.babelrc](./.babelrc)下载到到项目根目录



## 高级内容

### React

掌握常用 flow 语法（开发时根据注释，动态提示变量类型是否错误。类似eslint）

界面类返回 Function 或 继承 React.Component 的Class 的差异（Class有状态、也有生命周期，但是效率没有Function高。所以Function常见为简单无状态控件）

Function 和 继承Component的类 生命周期分别是什么情况

了解界面刷新逻辑，如何减少刷新频率缩小需要刷新的界面范围（使用PureComponent 或 重写 shouldComponentUpdate方法）

利用requestAnimationFrame优化操作体验

服务端渲染和SEO(搜索引擎优化)



### Flow

flow是一套使用注解方式匹配参数和返回值的变量类型



### Redux

哪些界面需要使用 connect ，了解Redux刷新机制，优化界面刷新逻辑



### reselect

带有cache的state数据选择器。能优化数据获取效率。

https://github.com/reactjs/reselect



### isomorphic-fetch

dva封装的第三方网络库

https://github.com/matthew-andrews/isomorphic-fetch



###[微信小程序](./MiniProgram.md)



## 扩展部分（不要求掌握）

1. babel 将高版本语法转译为低版本支持的语法，增加代码兼容性
2. eslint 语法检测工具，提示代码格式、语法是否正确等
3. webpack 项目自动打包工具，需要了解代码打包原理和相关配置参数。js拆分和动态加载。
4. [dva第三方框架选择说明](https://github.com/sorrycc/blog/issues/1)
5. [autoprefixer](https://github.com/postcss/autoprefixer) 自动生成对应浏览器css样式
6. [react-move](http://website.c262fc49e10c147f48fbf9c9cb63fe5bc.cn-shanghai.alicontainer.com) react动画库
7. 性能测试工具 [react-addone-perf](https://github.com/facebook/react/blob/master/docs/docs/addons-perf.md) [中文参考](http://wiki.jikexueyuan.com/project/react/performance-tools.html)  
8. [几个最流行的React框架](https://hackernoon.com/the-coolest-react-ui-frameworks-for-your-new-react-app-ad699fffd651)
9. ​