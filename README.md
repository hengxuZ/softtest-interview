## 为什么要创建这个仓库？💪


👶小时候学习的经历告诉我，当学会了某个单一的知识点需要通过例题对它的概念以及用进行考察，以助于我能更好的掌握理解。

当一个章节学完后✍，还是通过例题对这个章节所涉及的知识点进行考察，从点到面的考察，将这些知识点贯穿起来，达到对知识点的更深入的理解。

相同地，我认为测试学习过程中，习题是至关重要的一部分，所以我收集了全网对应章节的笔试，面试题进行解答。📗

不定时更新面试题📚。为我自己加深知识点的同时，也希望能够给其他小伙伴带来便利。希望每个小伙伴都能学有所获，学以致用，然后能够取得自己心仪的offer👍

除此之外，还会不定期更新 **测试内推岗** **测试学习资源**
### java篇

- [Java学习+面试指南](https://github.com/Snailclimb/JavaGuide)

### 大厂技术博客

-[美团技术团队-测试](https://tech.meituan.com/tags/%E6%B5%8B%E8%AF%95.html)

-[百度QA](http://qa.baidu.com/)




### 网络篇
### linux篇
<details>
<summary>Cookie与Session的区别</summary>

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

### 项目篇

--- 
### 软件测试(大厂)面经
[ 测试老兵进阶突破，成功挑战大厂 P7 Offer！](https://mp.weixin.qq.com/s?__biz=MzU3NDM4ODEzMg==&mid=2247486213&idx=1&sn=154bc75fa8e891795a7cc2aa2b665ac3&chksm=fd3269ceca45e0d800bd2e938271f178d7362cc49113380abbf191aed81787403a72f91073a2&mpshare=1&scene=24&srcid=0519hctPH6WJUTT6G6iAldDS&sharer_sharetime=1589878431661&sharer_shareid=9ce364c7bb4eb26eb95b7a9f0a6f961a&key=6f25b447608369f09c0ffbc4f1f54accd3ed17d0e7c3a64397d1cc5752f2db2924b918f41aba470d2e89039532a18d5339bb48baf15e9be8eef0e299d96390c3dcfccababff389efe521b02b1ffcdf31&ascene=14&uin=MjEwOTkwMjM1&devicetype=Windows+7+x64&version=62090070&lang=zh_CN&exportkey=A01YqOCeg%2BXyEnOtQobQRzU%3D&pass_ticket=E%2BuXnmfm0gMw%2BzqmBUSwSq7NQqA825McIyEf%2BVDbD4M%3D)

[阿里测试开发5面面经](https://www.nowcoder.com/discuss/91278?type=2&order=3&pos=7&page=1)

[学而思测开面经（已offer）](https://www.nowcoder.com/discuss/429289)

[百度测试开发岗位面试题目回顾](https://juejin.im/post/5e57305fe51d4526f65cc62e)