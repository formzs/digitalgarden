---
{"dg-publish":true,"permalink":"//spring-boot/"}
---

## 1.1 简介
springboot 是 spring 家族中的一个全新框架，用来简化 spring 程序的创建和开发过程。在以往我们通过 SpringMVC+Spring+Mybatis 框架进行开发的时候，我们需要配置 web.xml，spring 配置，mybatis 配置，然后整合在一起，而 springboot 抛弃了繁琐的 xml 配置过程，采用大量默认的配置来简化我们的 spring 开发过程。

SpringBoot 化繁为简，使开发变得更加的简单迅速。
## 1.2 特性
-   能够快速创建基于 spring 的程序
-   能够直接使用 Java main 方法启动内嵌的 Tomcat 服务器运行 springboot 程序，不需要部署 war 包
-   提供约定的 starter POM 来简化 Maven 配置，让 Maven 的配置变得简单
-   自动化配置，根据项目的 Maven 依赖配置，springboot 自动配置 spring、springmvc 等
-   提供了程序的健康检查功能
-   基本可以完全不使用 xml 配合文件，采用注解配置

# 创建 SpringBootController 类
```java
package com.bjpowernode.springboot.web; 
 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.ResponseBody; 
 
@Controller 
public class SpringBootController { 
 
 @RequestMapping(value = "/springBoot/say") 
 public @ResponseBody String say() { 
     return "Hello,springBoot!"; 
 } 
} 
```