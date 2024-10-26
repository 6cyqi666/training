---
Project-TrainingWithStudent
---
---
# 序言
## github绑定邮箱和用户名指令：
- git config --global user.name 
- git config --global user.email
## 检查是否绑定指令：
- git config --global --list
# 一. 项目环境配置

## 1. 后端数据库

### 1.1. 后端数据库

ip:
10.60.1.38:3306

### 1.2. 数据库客户端dbeaver

使用Dbeave来做客户端访问数据库。很好用。

如果出现错误：

Public Key Retrieval is not allowed

在下面这里设置一下连接参数：

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

## 2. 后端开发工具：Idea community

### 2.1. 使用idea intelij community

社区版在页面下部，滚动一下，在下面一行。

地址：[https://www.jetbrains.com/idea/download/?section=windows](https://www.jetbrains.com/idea/download/?section=windows)

### 2.2. mvn镜像源

maven是一个java项目，所以它的安装不分windows版本或者linux版本。只需要下载解压包解压。让ide指向使用它的路径即可。以及让环境变量指向它的bin路径即可。重要的是配置setting.xml，让它在中国大陆区域使用阿里云仓库。

maven不须安装的解压包下载地址：

[https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi)

设置配置文件

<?xml version="1.0" encoding="UTF-8"?>

<settingsxmlns="http://maven.apache.org/SETTINGS/1.2.0"

    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

    xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.2.0 https://maven.apache.org/xsd/settings-1.2.0.xsd">

<mirrors>

    `<mirror>`

    `<id>`aliyun-repo`</id>`

    `<mirrorOf>`central`</mirrorOf>`

    `<url>`https://maven.aliyun.com/repository/public`</url>`

    `<releases>`

    `<enabled>`true`</enabled>`

    `</releases>`

    `<snapshots>`

    `<enabled>`true`</enabled>`

    `</snapshots>`

    `</mirror>`

</mirrors>

  `<localRepository>`D:/Programes/java/mavenRepositery`</localRepository>`

<profiles>

    `<profile>`

    `<id>`default`</id>`

    `<activation>`

    `<activeByDefault>`true`</activeByDefault>`

    `</activation>`

    `<repositories>`

    `<repository>`

    `<id>`central`</id>`

    `<url>`https://repo.maven.apache.org/maven2`</url>`

    `<releases>`

  `<enabled>`true`</enabled>`

    `</releases>`

    `<snapshots>`

  `<enabled>`true`</enabled>`

    `</snapshots>`

    `</repository>`

    `</repositories>`

    `</profile>`

</profiles>

</settings>

在ideaintellij设置中让maven指向它的bin. 并且配置文件指向上面这个setting.xml

### 2.3. 下载依赖

项目是依赖，pom.xml类似package.json。 类似npm install . 后台项目使用mvn install来安装。

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg)

### 2.4. 当无法下载时

复制maven包，替代setting.xml中指定的本地仓库
。

## 3. 前端开发工具vscode

### 3.1. ant-design-cli

npm i @ant-design/pro-cli -g

（这个似乎是不需要的，没有测试太仔细）

### 3.2. 安装插件

安装gitlen

## 4. github命令

### 4.1. windows推送到github

已经使用token来设置windows, 不再使用用户名和密码。

在终端中运行 `<span lang="EN-US">git push</span>`时，会出现弹出框， 使用sign in with your browser. 在浏览器上认证后就可以使用。

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.jpg)

### 4.2. 切换多个github账户

此功能一般人忽略。

在windows上，如何切换自己的多个git账户。

控制面板====> 用户账户====>管理windows凭据====>git:https://github.com ：  删除。

删除后，在弹出上面的对话框时再重新登录。

### 4.3. 常用命令

在项目根目录下执行

git add .

git commit
-a -m 提交原因 --no-verify

git push

## 5. 后端框架

### 5.1. 通过postman初始化数据

使用接口

http://localhost:9090/user/save

带上json数据

{

  "name":"root",

  "username":"root",

  "password":"root"

}

这一步，通常不用执行，由开发权限的团队执行。

### 5.2. 运行springboot

找到

src/main/java/com/app/raghu/SpringBootRestSecurityJwtNewApplication.java

点击右键：

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.jpg)

## 6. 前端框架ant-design

ant.design 官网文档

[https://pro.ant.design/zh-CN/docs/overview](https://pro.ant.design/zh-CN/docs/overview)

### 6.1. 本地源安装依赖包

使用下面的本地源替代npm原来的阿里云镜像源

npm set registry [http://10.60.1.38:4873](http://10.60.1.38:4873)

npm config list

npm install

### 6.2. 运行

先安装

npm run dev

# 一. 项目环境配置

## 1. 后端数据库

### 1.1. 后端数据库

ip:
10.60.1.38:3306

### 1.2. 数据库客户端dbeaver

使用Dbeave来做客户端访问数据库。很好用。

如果出现错误：

Public Key Retrieval is not allowed

在下面这里设置一下连接参数：

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

## 2. 后端开发工具：Idea community

### 2.1. 使用idea intelij community

社区版在页面下部，滚动一下，在下面一行。

地址：[https://www.jetbrains.com/idea/download/?section=windows](https://www.jetbrains.com/idea/download/?section=windows)

### 2.2. mvn镜像源

maven是一个java项目，所以它的安装不分windows版本或者linux版本。只需要下载解压包解压。让ide指向使用它的路径即可。以及让环境变量指向它的bin路径即可。重要的是配置setting.xml，让它在中国大陆区域使用阿里云仓库。

maven不须安装的解压包下载地址：

[https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi)

设置配置文件

<?xml version="1.0" encoding="UTF-8"?>

<settingsxmlns="http://maven.apache.org/SETTINGS/1.2.0"

    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

    xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.2.0 https://maven.apache.org/xsd/settings-1.2.0.xsd">

<mirrors>

    `<mirror>`

    `<id>`aliyun-repo`</id>`

    `<mirrorOf>`central`</mirrorOf>`

    `<url>`https://maven.aliyun.com/repository/public`</url>`

    `<releases>`

    `<enabled>`true`</enabled>`

    `</releases>`

    `<snapshots>`

    `<enabled>`true`</enabled>`

    `</snapshots>`

    `</mirror>`

</mirrors>

  `<localRepository>`D:/Programes/java/mavenRepositery`</localRepository>`

<profiles>

    `<profile>`

    `<id>`default`</id>`

    `<activation>`

    `<activeByDefault>`true`</activeByDefault>`

    `</activation>`

    `<repositories>`

    `<repository>`

    `<id>`central`</id>`

    `<url>`https://repo.maven.apache.org/maven2`</url>`

    `<releases>`

  `<enabled>`true`</enabled>`

    `</releases>`

    `<snapshots>`

  `<enabled>`true`</enabled>`

    `</snapshots>`

    `</repository>`

    `</repositories>`

    `</profile>`

</profiles>

</settings>

在ideaintellij设置中让maven指向它的bin. 并且配置文件指向上面这个setting.xml

### 2.3. 下载依赖

项目是依赖，pom.xml类似package.json。 类似npm install . 后台项目使用mvn install来安装。

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg)

### 2.4. 当无法下载时

复制maven包，替代setting.xml中指定的本地仓库
。

## 3. 前端开发工具vscode

### 3.1. ant-design-cli

npm i @ant-design/pro-cli -g

（这个似乎是不需要的，没有测试太仔细）

### 3.2. 安装插件

安装gitlen

## 4. github命令

### 4.1. windows推送到github

已经使用token来设置windows, 不再使用用户名和密码。

在终端中运行 `<span lang="EN-US">git push</span>`时，会出现弹出框， 使用sign in with your browser. 在浏览器上认证后就可以使用。

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.jpg)

### 4.2. 切换多个github账户

此功能一般人忽略。

在windows上，如何切换自己的多个git账户。

控制面板====> 用户账户====>管理windows凭据====>git:https://github.com ：  删除。

删除后，在弹出上面的对话框时再重新登录。

### 4.3. 常用命令

在项目根目录下执行

git add .

git commit
-a -m 提交原因 --no-verify

git push

## 5. 后端框架

### 5.1. 通过postman初始化数据

使用接口

http://localhost:9090/user/save

带上json数据

{

  "name":"root",

  "username":"root",

  "password":"root"

}

这一步，通常不用执行，由开发权限的团队执行。

### 5.2. 运行springboot

找到

src/main/java/com/app/raghu/SpringBootRestSecurityJwtNewApplication.java

点击右键：

![](file:///C:/Users/YAOZON~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.jpg)

## 6. 前端框架ant-design

ant.design 官网文档

[https://pro.ant.design/zh-CN/docs/overview](https://pro.ant.design/zh-CN/docs/overview)

### 6.1. 本地源安装依赖包

使用下面的本地源替代npm原来的阿里云镜像源

npm set registry [http://10.60.1.38:4873](http://10.60.1.38:4873)

npm config list

npm install

### 6.2. 运行

先安装

npm run dev
