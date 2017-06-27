# Part I. Overview of Spring Framework 总览介绍
Spring Framework 是一个提供完善的基础设施用来支持来开发 Java 应用程序的 Java 平台。Spring 负责基础设施功能，而您可以专注于您的应用。

Spring 可以使你从“简单的Java对象”（POJO）构建应用程序，并且将企业服务非侵入性的应用到 POJO。此功能适用于 Java SE 编程模型和完全或者部分的 Java EE 。Spring 的设计是非侵入性的，也就是说你的领域逻辑代码一般对框架本身无依赖性。在你的集成层（如数据访问层），在数据访问技术和 Spring 的库一些依赖将存在。然而，它应该很容易从你的剩余代码中分离这些依赖。

Spring 是模块化的，允许你使用的你需要的部分，而不必把其余带进来。你可以在任何框架之上去使用IOC容器，但你也可以只使用 Hibernate 集成代码 或 JDBC 抽象层。Spring Framework 支持声明式事务管理，通过 RMI 或 Web 服务远程访问你的逻辑，并支持多种选择持久化你的数据。它提供了一个全功能的 MVC 框架，使您能够将 AOP 透明地集成到您的软件。

在很多的情况下使 Spring 是一个合理的选择，从资源受限的嵌入式程序到成熟的企业应用程序都可以使用 Spring。

### 典型的 Spring Web 应用程序
![](http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/images/overview-full.png)

Spring 声明式事务管理特性使 Web 应用程序拥有完全的事务，就像你使用 EJB 容器管理的事务。所有的自定义业务逻辑可以用简单的 POJO 实现，用 Spring 的 IoC 容器进行管理。额外的服务包括发送电子邮件和验证，是独立的网络层的支持，它可以让你选择在何处执行验证规则。Spring 的 ORM 支持集成 JPA，Hibernate，JDO；例如，当使用 Hibernate，您可以继续使用现有的映射文件和 标准的 Hibernate 的 SessionFactory 配置。表单控制器将 Web 层和领域模型无缝集成，消除 ActionForms 或其他类用于变换 HTTP 参数成为您的域模型值的需要。

### 集成第三方Web框架
![](http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/images/overview-thirdparty-web.png)

有时，不允许你完全切换到一个不同的框架。Spring Framework 不强制使用它,它不是一个全有或全无的解决方案。现有的前端 Struts, Tapestry, JSF 或其他 UI 框架，可以集成一个基于 Spring 中间件，它允许你使用 Spring 事务的功能。你只需要将业务逻辑连接使用 ApplicationContext 和使用WebApplicationContext 集成到你的 web 层。

### 远程访问服务实现
![](http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/images/overview-remoting.png)

当你需要通过 web 服务访问现有代码时，可以使用 Spring 的 Hessian-, Burlap-, Rmi- 或 JaxRpcProxyFactory 类。启用远程访问现有的应用程序并不难。

### 包装现有的POJO
![](http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/images/overview-ejb.png)

Spring Framework 也提供了 Enterprise JavaBeans 访问和抽象层使你能重用现有的 POJOs,并且在需要声明安全的时候打包他们成为无状态的 bean 用于可伸缩，安全的 web 应用里。

总的来说，作为一个应用程序的开发者，你可以从 Spring 平台获得以下好处：

* 使 Java 方法可以执行数据库事务而不用去处理事务 API。
* 使本地 Java 方法可以执行远程过程而不用去处理远程 API。
* 使本地 Java 方法可以拥有管理操作而不用去处理 JMX API。
* 使本地 Java 方法可以执行消息处理而不用去处理 JMS API。
