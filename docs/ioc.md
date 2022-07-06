# IOC

控制反转和依赖注入

控制反转（Inversion of Control，缩写IOC）是面向对象编程中的一种设计原则，
可以用来减低计算机代码之间的耦合度。其中最常见的方式叫做依赖注入（Dependency Injection
简称DI）。通过控制反转，对象在被创建的时候，由一个调控系统内所有对象的外界实体
所依赖的对象的引用传递给它。也可以说，依赖被注入到对象中。

## 文件介绍

controller: 处理http请求以及调用service层的处理方法
module：处理其他类的引用与共享
service：封装通用的业务逻辑、与数据层的交互、其他额外的三方请求
main.ts：入口文件，使用`NestFactory`用来创建Nest应用实例


## 生成文件不带单元测试

在`nest-cli.json`中添加
```
"generateOptions": {
  "spec": false
}
```