# spring-mvc-demo

```
一个空的SpringMvc项目工程
```

## 用途

1. webApp项目工程搭建
2. webService项目工程搭建

## 说明

1. 项目针对App应用和Service应用搭建。可能会针对不同的应用，多引用了一些Jar包。可根据自身项目需求，从Pom文件中删除不需要的Jar包。
2. 下载项目需在pom.xml和web.xml中修改自己的项目名称。

## 需修改的文件
1. pom.xml 修改项目名称、报名成、打包方式
```
<groupId>cn.com.custom</groupId>
	<artifactId>spring-mvc-demo</artifactId>
<packaging>war</packaging>
```
2. web.xml 修改Spring-mvc-demo为自己的项目名称
```

<context-param>
	<param-name>webAppRootKey</param-name>
	<param-value>spring-mvc-demo.root</param-value>
</context-param>


<servlet>
	<servlet-name>spring-mvc-demo</servlet-name>
	<servlet-class>
		org.springframework.web.servlet.DispatcherServlet
	</servlet-class>
	<init-param>
		<param-name>contextConfigLocation</param-name>
		<param-value>WEB-INF/spring-mvc.xml</param-value>
	</init-param>
	<load-on-startup>3</load-on-startup>
</servlet>
	
<servlet-mapping>
	<servlet-name>spring-mvc-demo</servlet-name>
	<url-pattern>*.html</url-pattern>
</servlet-mapping>
```
