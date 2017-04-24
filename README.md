[TOC]

## 初级内容

### 工具



### js基本语法

this绑定的意义





### es5  es6

http://es6.ruanyifeng.com/ 章节列表上方中文的部分
(简介、转码器可以不用看)

重点：
let const
解构
Promise
await 
yield





### React(View框架)

jsx

import 和 require 的异同点



备注：

1. 页面、组件在jsx中必须首字母大写。只有浏览器自带组件（如：div、a、img）才使用首字母小写。
2. xxx







### Flux(和MVC不同的设计思想)

```
<img src="./img/flux.jpg" />
```

Store： 整个程序的状态中心（存储各个勾选框是否勾选，当前显示的页面是什么页面）

React View： View层，根据Store中的状态显示当前界面样式(如：Store中存储现在显示第二页，View根据这个状态显示第二页)

Action Creators： 逻辑层，根据用户点击处理逻辑，并发出对Store状态变化的请求。（如：用户下拉加载更多，发起网络更新数据，并根据获取到的数据，发出需要对Store新增数据的请求）

Dispatcher： 根据Action发来的修改请求，修改Store的数据，并由Store触发View的自动刷新



Flux的数据流向单一，不会出现A点击改变B状态，B点击后又修改C状态，又提交数据，这种复杂情况。所有事件统一用Action的方式修改Store，再由Store统一修改界面显示。



参考文档

http://www.ruanyifeng.com/blog/2016/01/flux.html





### Redux(Controller框架)

Redux是Flux设计思想的具体实现，需要先了解Flux

Redux封装了Flux各个模块之间对接的方法，只需要分别编写相关模块并绑定Redux。



connect: 绑定Store和View，并且支持对View需要的数据进行筛选

dispatch: 提交Action给Dispatcher

注册reducer: 接收Action，并修改Store



```
学到这可以尝试跑通dva的example
https://github.com/sorrycc/blog/issues/18
```





### ant.design  蚂蚁金服类库





### react-router 被蚂蚁金服封装在内的页面跳转类库

版本号和使用方法跟随dva引用的版本，目前版本2.8.1

文档地址： https://github.com/ReactTraining/react-router/tree/v2.8.1

API文档地址： https://github.com/ReactTraining/react-router/blob/v2.8.1/docs/API.md

API中文地址（需要参考英文文档）： http://react-guide.github.io/react-router-cn/index.html



[Route 相互嵌套情况界面会被嵌套显示](https://github.com/reactjs/react-router-tutorial/blob/master/lessons/04-nested-routes/README.md)

匹配优先级

[带参地址的匹配方法](https://github.com/reactjs/react-router-tutorial/blob/master/lessons/06-params/README.md)

[页面跳转标签 Link](https://github.com/reactjs/react-router-tutorial/blob/master/lessons/03-navigating-with-link/README.md)

[URL重定向](https://github.com/ReactTraining/react-router/blob/v2.8.1/docs/API.md#redirect)

[IndexRoute 的使用](https://github.com/reactjs/react-router-tutorial/blob/master/lessons/08-index-routes/README.md)

[用代码进行页面跳转](https://github.com/ReactTraining/react-router/blob/v2.8.1/docs/API.md#routercontext)



```
根据 ant 的使用方法新建demo工程，需要完成以下功能：
1. 新建页面，实现点击按钮计数器加1、减1、清空功能，需要使用redux实现
2. 新建页面，实现获取首页源码字符串，并在首页显示的功能
3. 以上页面的点击按钮和相关界面，使用ant类库提供的样式
```





### git基本操作 

安装并会使用 GitHub Desktop

add

commit

push

PR (发起分支合并请求)

冲突解决





### js代码调试方法

js代码中嵌入“debugger”关键字，代码端断点

浏览器调试模式打断点

js未捕获异常自动断点调试（高级用法：无论是否捕获都自动断点调试）





### css 

基本样式

block  inline-block 

flex 

float





### jest

js单元测试工具

详见jest.md





## 高级内容

### React

掌握常用 flow 语法（开发时根据注释，动态提示变量类型是否错误。类似eslint）

界面类返回 Function 或 继承 React.Component 的Class 的差异（Class有状态、也有生命周期，但是效率没有Function高。所以Function常见为简单无状态控件）

Function 和 继承Component的类 生命周期分别是什么情况

了解界面刷新逻辑，如何减少刷新频率缩小需要刷新的界面范围（使用PureComponent 或 重写 shouldComponentUpdate方法）

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





## 扩展部分（不要求掌握）

1. babel 将高版本语法转译为低版本支持的语法，增加代码兼容性
2. eslint 语法检测工具，提示代码格式、语法是否正确等
3. webpack 项目自动打包工具，需要了解代码打包原理和相关配置参数。js拆分和动态加载。
4. [dva第三方框架选择说明](https://github.com/sorrycc/blog/issues/1)
5. xx