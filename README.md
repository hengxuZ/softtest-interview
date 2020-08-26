## 测试开发每日一练📆

### 以面试题来驱动学习，每天进步一点！🎉

- 题目均来自**测试开发**岗的大厂真实面试题

- 除此之外，还会不定期更新 **测试内推岗** **测试学习资源**🍻
### 使用建议
> 在阅读题目时，先自我思考一下🤔。然后再点击题目即可查看答案或百度。

---

### 测试篇
<details>
<summary>01.白盒和黑盒测试的方法有哪些？</summary>

- 黑盒测试的测试方法有：等价类划分、边界值分析法、猜错法、随机数法、因果图。
- 白盒测试的测试方法有：代码检查法、程序变异、静态结构分析法、静态质量度量法、符号测试法、逻辑覆盖法、域测试、Z路径覆盖和基本路径测试法。
</details>

### java篇
<details>
<summary>01.数组、list与arrayList区别</summary>

1. 数组与ArrayList区别
    - 数组是在内存空间中申请一段连续的内存地址，所以数组的查询速度很快是常量
    - ArrayList的大小是按照其中存储的数据来动态扩充与收缩的。所以，我们在声明ArrayList对象时并不需要指定它的长度

2. List与ArrayList区别
    -  List类是ArrayList类的**泛型等效类**
        - 由于ArrayList可以插入不同类型的数据，因为ArrayList都把他们当作了object来处理。
            - 在我们使用ArrayList中的数据来处理问题的时候，很可能会报类型不匹配的错误，也就是说**ArrayList不是类型安全**
            - 并且这里涉及了装箱和拆箱导致**ArrayList处理性能低**
                - 装箱：将值类型的数据打包到引用类型的实例中
                - 拆箱：从引用数据中提取值类型
        - List继承了Arraylist，在定义时需要加上特定的类型，这样就不会引起强制转换，类型检测也交给编译器进行检测

</details>
<details>
<summary>JDK、JVM、JRE是什么?</summary>

- JVM
    - Java 虚拟机（JVM）是运行 Java 字节码的虚拟机。JVM 有针对不同系统的特定实现（Windows，Linux，macOS），目的是使用相同的字节码，它们都会给出相同的结果。
    > 在 Java 中，JVM 可以理解的代码就叫做字节码（即扩展名为 .class 的文件），它不面向任何特定的处理器，只面向虚拟机。Java 语言通过字节码的方式，在一定程度上解决了传统解释型语言执行效率低的问题，同时又保留了解释型语言可移植的特点。所以 Java 程序运行时比较高效，而且，由于字节码并不针对一种特定的机器，因此，Java 程序无须重新编译便可在多种不同操作系统的计算机上运行。

- JDK
    - JDK 是 Java Development Kit，它是功能齐全的 Java SDK。它拥有 JRE 所拥有的一切，还有编译器（javac）和工具（如 javadoc 和 jdb）。它能够创建和编译程序。
- JRE
    - JRE 是 Java 运行时环境。它是运行已编译 Java 程序所需的所有内容的集合，包括 Java 虚拟机（JVM），Java 类库，java 命令和其他的一些基础构件。但是，它不能用于创建新程序。

>如果你只是为了运行一下 Java 程序的话，那么你只需要安装 JRE 就可以了。如果你需要进行一些 Java 编程方面的工作，那么你就需要安装 JDK 了。但是，这不是绝对的。有时，即使您不打算在计算机上进行任何 Java 开发，仍然需要安装 JDK。例如，如果要使用 JSP 部署 Web 应用程序，那么从技术上讲，您只是在应用程序服务器中运行 Java 程序。那你为什么需要 JDK 呢？因为应用程序服务器会将 JSP 转换为 Java servlet，并且需要使用 JDK 来编译 servlet。

</details>

### python篇
<details>
<summary>01如何使用python实现多线程</summary>

> 通过python提供的threading模块

```python
import time, threading

# 新线程执行的代码:
def loop():
    print('thread %s is running...' % threading.current_thread().name)
    n = 0
    while n < 5:
        n = n + 1
        print('thread %s >>> %s' % (threading.current_thread().name, n))
        time.sleep(1)
    print('thread %s ended.' % threading.current_thread().name)

print('thread %s is running...' % threading.current_thread().name)
t = threading.Thread(target=loop, name='LoopThread')
t.start()
t.join()
print('thread %s ended.' % threading.current_thread().name)
```

</details>

### 数据库
<details>
<summary>01.数据库的范式</summary>

1. 第一范式NF：
    - 数据库表中的字段都是单一属性的，不可再分。简单的说，每一个属性都是原子项，不可分割
2. 第二范式2NF
    - 数据库表中不存在非关键字段对任一候选关键字段的部分函数依赖，即符合第二范式
3. 第三范式3NF   
    - 数据表中如果不存在非关键字段对任一候选关键字段的传递函数依赖则符合3NF
- [参考文章](https://blog.csdn.net/h330531987/article/details/71194540)
</details>

<details>
<summary>02.mysql常用的存储引擎有什么？区别是什么？</summary>

1. 常用的存储引擎是：InnoDB，MyISAM

2. 区别在于：
    - InnoDB支持事务，而MyISAM不支持事务
    - InnoDB支持行级锁，而MyISAM支持表级锁
    - InnoDB支持MVC, 而MyISAM不支持
    - InnoDB支持外键，而MyISAM不支持
    - InnoDB不支持全文索引，而MyISAM支持。
</details>

### 网络通信篇
<details>
<summary>01.Cookie与Session的区别</summary>

> HTTP是无状态协议，它不对之前发生过的请求和响应的状态进行管理。也就是说，无法根据之前的状态进行本次的请求处理。HTTP/1.1虽然是无状态协议，但为了实现期望的保持状态功能，于是引入了Cookie技术。
- 隐私策略与安全策略不同
    - Cookie:存储在客户端(浏览器)，能被用户看见或使用。可能会被用于xss(跨站脚本攻击)
    - Session:存储服务端，相对更加安全
- 有效期不同
    - Cookie:通过Expires字段来设置过期时间
    - Session:关闭浏览器后，服务器存储的Session就会失效，为了保障浏览器内存不溢出
- 服务器压力不通
    - Cookie:存储在客户端，不占用服务端资源。但每次请求都会带上Cookie，对带宽造成一定浪费
    - Session:存储在服务端，每个用户都会产生一个Session。假如并发访问的用户十分多，会产生十分多的Session，耗费大量的内存。
</details>

<details>

<summary>02.打开浏览器，从输入 www.baidu.com 到看到浏览器显示页面，这个过程中，都有哪些步骤和环节？</summary>


1. DNS域名解析
2. TCP三次握手
3. 发生http请求
4. 接受http响应
5. 浏览器解析响应文件(js,css,html)

[参考文章](https://segmentfault.com/a/1190000006879700)

</details>

### linux篇
<details>
<summary>查询文件中某个字符出现的次数，使用linux命令写出来</summary>

1. 底线命令模式
    - :%s/str//ng      

2. 文本查找模式
    - grep -o str filename | wc -l

</details>

### 编程算法题

<details>
<summary>01.你能手写一下冒泡排序吗？</summary>

```python
def bubble_sort(list):
    for i in range(0,len(list)-1):
        for j in range(i+1,len(list)):
            if list[i]>list[j]:
                list[j],list[i] = list[i],list[j]
    return list  
```
</details>
<details>
<summary>02.在字符串中找出连续最长的字符串，并把这个串的长度返回，
    譬如“abcdabce" 最长串为abcd或者abce，长度为4</summary>

```python

```
</details>



--- 
## 资料分享🗓
- [sql在线练习网站](https://sqlzoo.net/)
### 大厂技术博客👍

- [美团技术团队-测试](https://tech.meituan.com/tags/%E6%B5%8B%E8%AF%95.html)

- [百度QA](http://qa.baidu.com/)


### 软件测试(大厂)面经
- [Java学习+面试指南](https://github.com/Snailclimb/JavaGuide)
- [ 测试老兵进阶突破，成功挑战大厂 P7 Offer！](https://mp.weixin.qq.com/s?__biz=MzU3NDM4ODEzMg==&mid=2247486213&idx=1&sn=154bc75fa8e891795a7cc2aa2b665ac3&chksm=fd3269ceca45e0d800bd2e938271f178d7362cc49113380abbf191aed81787403a72f91073a2&mpshare=1&scene=24&srcid=0519hctPH6WJUTT6G6iAldDS&sharer_sharetime=1589878431661&sharer_shareid=9ce364c7bb4eb26eb95b7a9f0a6f961a&key=6f25b447608369f09c0ffbc4f1f54accd3ed17d0e7c3a64397d1cc5752f2db2924b918f41aba470d2e89039532a18d5339bb48baf15e9be8eef0e299d96390c3dcfccababff389efe521b02b1ffcdf31&ascene=14&uin=MjEwOTkwMjM1&devicetype=Windows+7+x64&version=62090070&lang=zh_CN&exportkey=A01YqOCeg%2BXyEnOtQobQRzU%3D&pass_ticket=E%2BuXnmfm0gMw%2BzqmBUSwSq7NQqA825McIyEf%2BVDbD4M%3D)

- [阿里测试开发5面面经](https://www.nowcoder.com/discuss/91278?type=2&order=3&pos=7&page=1)

- [学而思测开面经（已offer）](https://www.nowcoder.com/discuss/429289)

- [百度测试开发岗位面试题目回顾](https://juejin.im/post/5e57305fe51d4526f65cc62e)
