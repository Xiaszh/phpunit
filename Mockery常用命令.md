**mock**: 使用mock生成代理类对象，重新实现了被测对象并注入了\Mockery\MockInterface方法

```
$mock = \Mockery::mock('foo');  //创建mock空对象，并命名为foo
$mock = \Mockery::mock(); // 创建mock空对象, 不推荐使用
$mock = \Mockery::mock('MyClass'); // 针对类模拟
$mock = \Mockery::mock('MyInterface'); // 针对接口模拟
$mock = \Mockery::mock('MyClass, MyInterface, OtherInterface'); // 针对多个类和接口模拟
$mock = \Mockery::mock('MyClass')->makePartial(); // 默认情况下，只有mock方法可以调用，加上makePartial后，非mock方法会调用真实方法
```
**spy**: 对没有mock的方法的会真实调用，并且返回null

```
$spy = \Mockery::spy('MyClass');
$spy = \Mockery::spy('MyClass, MyInterface, OtherInterface');
```
****