# 5. 使用Spring进行面向切面编程

面向切面编程（AOP）提供良一中思考程序结构的方式来补充面向对象编程（OOP）。面向对象中模块化的关键单元是类，而在AOP中，模块化单位是一个切面。切面使关注点模块化（例如事务管理），支持跨多种类型和对象的关注点。（这些关注点在AOP文献中通常被成为“跨领域”关注）。

Spring中一个关键的组件是AOP框架。虽然Spring IoC容器不依赖AOP（意味着如果不想使用AOP，就不需要），AOP对Spring IoC进行了补充，以提供功能非常强大的中间件解决方案。

**具有AspectJ切入点的Spring AOP**

*Spring 通过使用基于模式的方法或`@AspectJ 注解样式`提供了简单强大的方式来编写自定义切面。这两种方式提供了完全类型化的建议，并使用了Aspectj切入点语言，同时扔使用Spring AOP进行编织。*

*本章要讨论基于架构和基于`@AspectJ`的AOP支持。下一章将讨论递增AOP支持*

在Spring框架中，AOP被用来：

* 提供声明式的企业级服务。此类服务中最重要的是声明式事务管理`declarative transaction management`。

* 让用户实现自定义切面，通过AOP补充对OOP的使用。

*如果您只对通用声明性服务或其他预包装的声明性中间件服务（例如池）感兴趣，则无需直接使用Spring AOP，并且可以跳过本章的大部分内容。*

