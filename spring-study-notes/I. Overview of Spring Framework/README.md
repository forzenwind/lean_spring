# Part I. Overview of Spring Framework 总览介绍
Spring Framework 是一个提供完善的基础设施用来支持来开发 Java 应用程序的 Java 平台。Spring 负责基础设施功能，而您可以专注于您的应用。

Spring 可以使你从“简单的Java对象”（POJO）构建应用程序，并且将企业服务非侵入性的应用到 POJO。此功能适用于 Java SE 编程模型和完全或者部分的 Java EE 。Spring 的设计是非侵入性的，也就是说你的领域逻辑代码一般对框架本身无依赖性。在你的集成层（如数据访问层），在数据访问技术和 Spring 的库一些依赖将存在。然而，它应该很容易从你的剩余代码中分离这些依赖。