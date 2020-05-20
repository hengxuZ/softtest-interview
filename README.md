## 使用说明 

> 点击箭头查看答案(在点击之前您可以先自问自答)

### java基础篇
<details>
<summary>面向对象的特征：继承、封装和多态</summary>

- 封装（encapsulation，有时称为数据隐藏）。从形式上看，封装是将数据和行为组合在一个包中，并对对象的使用者隐藏了数据的实现方式。

-  继承（Inheritance）是面向对象实现软件复用的重要手段，当子类继承父类后，子类作为一种特殊的父类，将直接获得父类的属性和方法。在面向对象方法中，类之间共享属性和操作的机制称为**继承**

- 多态（Polymorphism）指的是子类对象可以直接赋给父类变量，但运行时依然表现出子类的行为特征，这意味着同一个类型的对象在执行同一个方法时，可能表现出多种行为特征。

</details>

<details>
<summary>final, finally, finalize 的区别</summary>

- final:关键字final指示常量。表示变量只能被赋值一次。一旦被赋值之后，就不能够再更改了。

- finally:用于回收try块里打开的一些物理资源（例如数据库连接、网络连接和磁盘文件等），这些物理资源都必须显式回收。
    > Java的垃圾回收机制不会回收任何物理资源，垃圾回收机制只能回收堆内存中对象所占用的内存

- finalize:在垃圾回收机制回收某个对象所占用的内存之前，来清理该对象资源。

</details>

### 软件测试工程师(大厂)面经
[ 测试老兵进阶突破，成功挑战大厂 P7 Offer！](https://mp.weixin.qq.com/s?__biz=MzU3NDM4ODEzMg==&mid=2247486213&idx=1&sn=154bc75fa8e891795a7cc2aa2b665ac3&chksm=fd3269ceca45e0d800bd2e938271f178d7362cc49113380abbf191aed81787403a72f91073a2&mpshare=1&scene=24&srcid=0519hctPH6WJUTT6G6iAldDS&sharer_sharetime=1589878431661&sharer_shareid=9ce364c7bb4eb26eb95b7a9f0a6f961a&key=6f25b447608369f09c0ffbc4f1f54accd3ed17d0e7c3a64397d1cc5752f2db2924b918f41aba470d2e89039532a18d5339bb48baf15e9be8eef0e299d96390c3dcfccababff389efe521b02b1ffcdf31&ascene=14&uin=MjEwOTkwMjM1&devicetype=Windows+7+x64&version=62090070&lang=zh_CN&exportkey=A01YqOCeg%2BXyEnOtQobQRzU%3D&pass_ticket=E%2BuXnmfm0gMw%2BzqmBUSwSq7NQqA825McIyEf%2BVDbD4M%3D)

[阿里测试开发5面面经](https://www.nowcoder.com/discuss/91278?type=2&order=3&pos=7&page=1)

[学而思测开面经（已offer）](https://www.nowcoder.com/discuss/429289)

[百度测试开发岗位面试题目回顾](https://juejin.im/post/5e57305fe51d4526f65cc62e)