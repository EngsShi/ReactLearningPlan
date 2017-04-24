## jest

### [jest基础使用方法](http://facebook.github.io/jest/)



### 查看代码覆盖率

jest --coverage



### 生成、对比快照

注： 第一次运行自动生成快照，之后运行将会和第一次的快照进行比对
expect(tree).toMatchSnapshot();



### 刷新快照内容

jest -u 



## enzyme

模拟实际环境，生成虚拟节点

http://airbnb.io/enzyme/



### shallow 虚拟渲染

1. 子节点将会按照节点名称显示，不展开
2. 并且只会运行render，没有生命周期相关方法

http://airbnb.io/enzyme/docs/api/shallow.html



### mount 完整渲染

1. 子节点将会被展开
2. 会模拟DOM节点，并能做模拟操作
3. 会模拟生命周期相关方法

http://airbnb.io/enzyme/docs/api/mount.html