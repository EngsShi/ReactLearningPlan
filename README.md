## 初级内容

### [开发工具](Tools.md)



### css

[多种居中方法](https://www.jianshu.com/p/b0ba06d5dcfb) (注意兼容性问题)

[flex布局](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html) (注意：仅支持高级浏览器)

[display](http://www.w3cplus.com/css/how-well-do-you-know-display.html) (重点： block,inline-block)



### js基本语法

[this绑定的意义](https://segmentfault.com/a/1190000007101339)

[import 和 require 的异同点](https://www.cnblogs.com/crazycode2/p/11006933.html)



### es5  es6

[阮一峰的es6入门文章](http://es6.ruanyifeng.com/) (需要看的章节：2-9、11、14-20、24)

[es5版本Array新增方法](http://www.zhangxinxu.com/wordpress/2013/04/es5%E6%96%B0%E5%A2%9E%E6%95%B0%E7%BB%84%E6%96%B9%E6%B3%95/)



重点：
let const
解构
Promise
await 
[yield](http://es6.ruanyifeng.com/#docs/generator#yield--表达式) [处理异步方法使用co库](http://es6.ruanyifeng.com/#docs/generator-async#co-模块) 



### Node基础操作

命令行执行： node [js文件名]

[package.json配置文件常用参数](http://javascript.ruanyifeng.com/nodejs/packagejson.html)

安装依赖： npm init

添加依赖： npm install xxx

执行脚本： npm run xxx

安装依赖： yarn

添加依赖： yarn add xxx

执行脚本： yarn run xxx



### React(界面层框架)

jsx语法



备注：

1. 页面、组件在jsx中必须首字母大写。只有浏览器自带组件（如：div、a、img）才使用首字母小写。
2. xxx




### [Flux](Flux.md) 设计思想



### Redux(Controller框架)

Redux是Flux设计思想的具体实现，需要先了解Flux

Redux封装了Flux各个模块之间对接的方法，只需要分别编写相关模块并绑定Redux。



connect: 绑定Store和View，并且支持对View需要的数据进行筛选

dispatch: 提交Action给Dispatcher

注册reducer: 接收Action，并修改Store



配合 [react-addons-update](https://github.com/facebook/react/blob/master/docs/docs/addons-update.md) 插件更新数据，保证变更state时是创建而不是修改，并且优化创建效率



> 尝试跑通dva的example
> https://github.com/sorrycc/blog/issues/18



### [ant.design](https://ant.design)

蚂蚁金服基于React的界面组件库



注意： 2.x版本仅支持IE10以上，1.x版本兼容IE8



### [react-router](react-router.md)

第三方页面跳转类库，antd库已内置该类库2.x版本



> 根据 ant 的使用方法新建demo工程，需要完成以下功能：
>
> 1. 参考上个example创建新工程
> 2. 新建页面1，实现点击按钮计数器加1、减1、清空功能，需要使用redux实现
> 3. 新建页面2，实现获取测试工程首页源码字符串，并在当前页面中显示源码
> 4. 以上页面的点击按钮和相关界面，使用ant类库提供的样式



### git基本操作 

安装并会使用 GitHub Desktop

理解branch、remote、add、commit、push、pull、pull request(提交分支合并请求)

解决代码冲突问题



### js代码调试方法

[常用调试方法](http://www.runoob.com/w3cnote/js-debugging-skills.html) (debugger、浏览器调试模式打断点  等)

[未被捕获的异常自动断点](https://developers.google.cn/web/tools/chrome-devtools/console/track-exceptions?hl=zh-cn)（高级用法：无论是否被捕获都自动断点调试）



### [TypeScript](https://www.tslang.cn/docs/home.html)



### [jest](Jest.md)

js单元测试工具



> 对之前创建的工程编写测试脚本，要求：
>
> 1. 为redux方法编写测试用例，覆盖：加1、减1、清空、获取测试工程首页源码。(注：只需要对models中的相关方法进行测试，不需要执行dispatch)
> 2. 用快照接口(toMatchSnapshot)，分别为 增减界面 和 显示源码页 面编写测试用例
>
> 注： 让测试用例支持“imoprt”方法，需要将[.babelrc](./.babelrc)下载到到项目根目录



### UmiJs

[英文文档](https://umijs.org/docs)

> 尝试跑通umi的example
> (https://www.yuque.com/umijs/umi/bmvfg6)



## 高级内容

### React

界面类返回 Function 或 继承 React.Component 的Class 的差异（Class有状态、也有生命周期，但是效率没有Function高。所以Function常见为简单无状态控件）

Function 和 继承Component的类 生命周期分别是什么情况

了解界面刷新逻辑，如何减少刷新频率缩小需要刷新的界面范围（使用PureComponent 或 重写 shouldComponentUpdate方法）

利用requestAnimationFrame优化操作体验

[Hook](https://react.docschina.org/docs/hooks-intro.html) 是 React 16.8 的新增特性。它可以让你在不编写 class 的情况下使用 state 以及其他的 React 特性。

[How to fetch data with React Hooks?](https://www.robinwieruch.de/react-hooks-fetch-data)

### [Flow](https://flow.org)

用注释方式设置和检测变量类型和方法返回值类型是否正确



### Redux

1. [redux优化](https://juejin.im/post/596db2f9f265da6c4602ffc3?utm_source=gold-miner&utm_medium=readme&utm_campaign=github)
2. [数据扁平化操作，提高数据复用率](https://github.com/paularmstrong/normalizr) ([中文教程](https://yq.aliyun.com/articles/3168))



### reselect

带有cache的state数据选择器。能优化数据获取效率。

https://github.com/reactjs/reselect



### isomorphic-fetch

dva封装的第三方网络库

https://github.com/matthew-andrews/isomorphic-fetch



### [Less](https://less.bootcss.com/)

css预处理语言（带变量和参数的css生成脚本）



### [Babel](https://www.babeljs.cn/)

将高级版本js的方法转换成低级语法的工具。如：foreach、Map、async等高级语法。

需要知道怎么配置和使用Babel，并且了解不同版本js的语法差别。



### [Polyfill](https://blog.csdn.net/qq_42095204/article/details/100065972)

与Babel完成相同功能，但是Babel是将代码编译成低级语法，Polyfill是动态创建和添加高级语法代码到浏览器全局环境。



### [ESLint](https://eslint.bootcss.com/)

js代码规范检测工具，可以配置检测策略。

需要理解并且知道怎么修改ESLint参数。





### [微信小程序](./MiniProgram.md)





## 扩展部分（不要求掌握）

1. [手机端3种ViewPort的关系](http://www.cnblogs.com/2050/p/3877280.html) ([蚂蚁金服的说明文章](https://github.com/ant-design/ant-design-mobile/wiki/viewport%E8%AF%A6%E8%A7%A3))
2. webpack 项目自动打包工具，需要了解代码打包原理和相关配置参数。js拆分和动态加载。
3. [dva第三方框架选择说明](https://github.com/sorrycc/blog/issues/1)
4. [autoprefixer](https://github.com/postcss/autoprefixer) 自动生成对应浏览器css样式
5. [react-move](http://website.c262fc49e10c147f48fbf9c9cb63fe5bc.cn-shanghai.alicontainer.com) react动画库
6. 性能测试工具 [react-addone-perf](https://github.com/facebook/react/blob/master/docs/docs/addons-perf.md) [中文参考](http://wiki.jikexueyuan.com/project/react/performance-tools.html)  
7. [几个最流行的React框架](https://hackernoon.com/the-coolest-react-ui-frameworks-for-your-new-react-app-ad699fffd651)
8. 16版本新增的[React Fiber](https://segmentfault.com/a/1190000007376242功) [(扩展内容)](https://zhuanlan.zhihu.com/p/26027085) 功能，重构了底层页面刷新方法
9. 推荐的[项目文件结构](https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1)
10. [redux性能优化](https://juejin.im/entry/58eb2fb0570c350057dd921a?utm_source=gold-miner&utm_medium=readme&utm_campaign=github)
11. 服务端渲染和SEO(搜索引擎优化)
12. [css常用布局介绍](https://juejin.im/post/5a22d0086fb9a0451a7631ee)
13. [移动端兼容问题](https://www.cnblogs.com/luckyXcc/p/6237933.html)
14. [React应用架构设计指南](https://zhuanlan.zhihu.com/p/32481579?group_id=930373272135118848)
15. [傻瓜函数式编程](https://github.com/justinyhuang/Functional-Programming-For-The-Rest-of-Us-Cn/blob/master/FunctionalProgrammingForTheRestOfUs.cn.md)

