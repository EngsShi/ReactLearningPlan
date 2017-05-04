## jest

### [jest基础使用方法](http://facebook.github.io/jest/)

[中文说明](http://www.ruanyifeng.com/blog/2016/02/react-testing-tutorial.html)



### 查看代码覆盖率

jest --coverage



### 生成、对比快照

注： 第一次运行自动生成快照，之后运行将会和第一次的快照进行比对
expect(tree).toMatchSnapshot();



### 刷新快照内容

jest -u 



### dva环境进行测试需要额外配置

1. 将[文件](./tests/setup.js)复制到项目的指定位置：  ./tests/setup.js
2. Package.json增加配置:

```
"jest": {
  "setupFiles": [
  	"./tests/setup.js"
  ]
}
```



## [enzyme](http://airbnb.io/enzyme/)

模拟实际环境，生成虚拟节点



### [shallow 虚拟渲染](http://airbnb.io/enzyme/docs/api/shallow.html)

1. 子节点将会按照节点名称显示，不展开
2. 并且只会运行render，没有生命周期相关方法



### [mount 完整渲染](http://airbnb.io/enzyme/docs/api/mount.html)

1. 子节点将会被展开，并最终返回真实节点
2. 会模拟DOM节点，并能做模拟操作
3. 会模拟生命周期相关方法



### 使用enzyme-to-json进行快照序列化测试

1. 引入类库：yarn add —dev enzyme-to-json
2. package.json增加配置项

```
"jest": {
  "snapshotSerializers": [
  	"enzyme-to-json/serializer"
  ]
}
```

3. 正常调用快照方法

```
import { shallow } from 'enzyme';

// 由于引用了redux的connect，此处必须这么写,跳过相关方法
const Click = require('./Click').WrappedComponent;

const component = shallow(
	<Click/>
);
expect(component).toMatchSnapshot();
```