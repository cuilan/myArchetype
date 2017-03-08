# myArchetype

## 步骤一
从maven官方提供的archetype模板中获取并创建自己的archetype，运行命令：
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
根据myArchetype创建自己的maven工程：
```java
mvn  archetype:generate
-DarchetypeGroupId=your.package.xxx
-DarchetypeArtifactId=myArchetype
-DarchetypeVersion=1.0.0
-DgroupId=your.package.xxx
-DartifactId=XXX
–DinteractiveMode=false
```
