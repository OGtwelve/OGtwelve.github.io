1.Spring Boot 入门

​	Spring简介:

​	简化Spring应用开发的一个框架

​	整个Spring技术栈的一个大整合



​	SpringBoot简化Spring,约定大于配置,去繁化简



背景:J2EE开发笨重,配置繁多,开发效率低下,第三方技术集成困难

SpringBoot-->J2EE一站式解决方案

SpringCloud->分布式整体解决方案



优点:

​	1.快速创建独立运行的Spring项目及主流的框架集成

​	2.使用嵌入式的servlet容器,应用无需打成war包

​	3.Strarters(启动器)自动依赖与版本控制

​	4.大量的自动配置,简化开发

​	5.无需配置XML,开箱即用

入门容易,精通难



2.微服务

​	微服务,架构风格(服务微化)

​	一个应用是一组小型服务,通过HTTP的方式进行互通



​	单体应用

​	所有东西(页面,代码)全部到放到一个应用中,运行时直接把整个项目打包成一个war包放到服务器运行

​	好处:

​			1.开发,测试简单,因为在一个应用中,不会牵扯到多个应用之间的互联,互调

​			2.部署也简单,直接把应用打包成war部署到服务器上即可

​			3.水平扩展也简单,当负载能力出现问题,将相同应用复制多份,都执行,通过负载均衡机制,提高并发能力

​	坏处:

​			1.牵一发动全身,可能因为一个小小的修改,就要重写部署,或者运行整个项目

​			2.项目需求过多,应用,分工合作,维护问题太大



SpringBoot版本仲裁中心

1.

2.启动器

![image-20201223193734280](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20201223193734280.png)

SpringBoot将所有的功能场景都抽取出,做成一个个的Starter(启动器),只需要在项目里导入需要用的启动器,所有的依赖都会被导入

3.@SpringBootConfiguration:SpringBoot配置类

​	标注在某个类上,说明这是一个SpringBoot配置类

​		@Configuration:配置类

​	@EnableAutoConfiguration:开启自动配置功能

​		以前需要我们自己配置的东西,SpringBoot帮我们自动配置

​		@AutoConfigurationPackage:自动配置包

​		@Import(Registrar.class):

​			注入一个组件,将主配置类所在包下,以及下面所有子包里面的组件全部扫描到Spring容器里

​	@EnableAutoConfigurationImportSelector:导入那些组件的选择器

有了自动配置类,免去了手动导入配置组件的工作



简单部署:

![image-20201224154911869](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20201224154911869.png)



打成jar包之后使用java -jar命令执行即可



YAML

YetAnotherMarkupLanguage(另一种标记语言)

YMAL 

Aint Markup Language(不只是标记语言)



标记语言:

​		之前的配置文件,大都是XML文件

​		YAML: 以数据为中心,写法简洁,不需要重复开闭标签

