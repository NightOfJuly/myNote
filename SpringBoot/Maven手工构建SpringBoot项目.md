# Maven手工构建SpringBoot项目

### 1.构建Maven项目

​	使用任意开发工具新建空的Maven项目。

### 2.修改pom.xml

1. 添加springboot的父级依赖

   ```
   	<!-- spring-boot-starter-parent 是一个特殊的starter，它用来提供相关的Maven默认依赖，
   		使用它后，常用的包依赖可以省去version标签 -->
   	<parent>
   		<groupId>org.springframework.boot</groupId>
   		<artifactId>spring-boot-starter-parent</artifactId>
   		<version>1.5.3.RELEASE</version>
   		<relativePath/> <!-- lookup parent from repository -->
   	</parent>
   ```

2. 在dependencies添加web支持的starter pom，这样就添加了web的依赖。

   ```
       <dependency>
           <groupId>org.springframework.boot</groupId>
           <artifactId>spring-boot-starter-web</artifactId>
       </dependency>
   ```

3. 添加springboot的编译插件

   ```
   	<build>
   		<plugins>
   			<plugin>
   				<groupId>org.springframework.boot</groupId>
   				<artifactId>spring-boot-maven-plugin</artifactId>
   			</plugin>
   		</plugins>
   	</build>
   ```

注：若使用里程碑版还需要一个repositories的配置，正式版则不需要。这里使用正式版就不写配置了。

## 启动项目

1.可以使用开发工具自带的Run，右键Run As 可以选择SpringBootAPP或者JavaApplication

2.可以通过Maven命令，运行项目，进入项目路径，使用命令：mvn spring-boot:run