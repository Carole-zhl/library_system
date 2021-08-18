# library_system

技术链 vue2 vuex express axios mysql

本来是通过node.js连接mysql，开启服务端，从而实现动态网页。

但是因为github只能放静态网页，只能把动态的改成静态了，所以这里看到的增删改查只是静态的，刷新就又初始化了

主要重点 

1.axios连接接口，服务端是用node.js连接mysql 实现增删改查 
        
2.vuex通过Store实现标签窗口与左边manual的同步显示，还有缓存的开关，以及因为浏览器刷新导致的store数据清空，通过存储到浏览器的sessionStorage中来解决
        
3.vue-router拦截，实现必须要登录才能进入页面，通过地址跳转无效。（实际使用过程中想到，真实的项目中是不是Axios拦截更安全点）
        
4.手写数据列表组件，窗口标签组件
        
  a.数据列表组件通过一个当前页面数组，一个总数组来实现数据界面的效果
  b.窗口标签组件通过store和缓存<keep-alive :include="setAlive">来实现
                        
5.服务端连接mysql数据库，用了一点express，学习了如何客户端时如何通过ajax接口连接到服务端，服务端又是如何处理数据，返回数据
