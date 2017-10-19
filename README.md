# springcloudconfig
spring-cloud-config
Spring Cloud会创建一个`Bootstrap Context`，作为Spring应用的`Application Context`的父上下文。
初始化的时候，`Bootstrap Context`负责从外部源加载配置属性并解析配置。
这两个上下文共享一个从外部获取的`Environment`。
`Bootstrap`属性有高优先级，默认情况下，它们不会被本地配置覆盖。 
`Bootstrap context`和`Application Context`有着不同的约定，所以新增了一个`bootstrap.yml`文件，而不是使用`application.yml` (或者`application.properties`)。保证`Bootstrap Context`和`Application Context`配置的分离。
