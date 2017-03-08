# myArchetype
使用 maven 创建自定义的 archetype 模板，自定义预置一些通用配置文件、公用的代码等，可快速生成个性化的 maven 工程。

## 步骤一
从 maven 官方提供的 archetype 模板中获取并创建自己的 archetype ，运行命令：
```java
mvn  archetype:generate
–DarchetypeGroupId=org.apache.maven.archetypes
–DarchetypeArtifactId=maven-archetype-archetype
–DgroupId=your.package.xxx
–DartifactId=myArchetype
–Dversion=1.0.0
–DinteractiveMode=false
```
## 步骤二
在`/src/main/resources/archetype-resources`目录下放入想要的`通用配置文件`、`web.xml`、`pom.xml`及`通用代码`。
## 步骤三
在`/src/main/resources/META-INF/maven/archetype.xml`中，编辑并配置放入的资源文件所属目录及从属关系。
## 步骤四
执行命令安装archetype到本地仓库：
```java
mvn  install
```
# 使用archetype
根据 myArchetype 创建自己的 maven 工程：
```java
mvn  archetype:generate
-DarchetypeGroupId=your.package.xxx
-DarchetypeArtifactId=myArchetype
-DarchetypeVersion=1.0.0
-DgroupId=your.package.xxx
-DartifactId=XXX
–DinteractiveMode=false
```
