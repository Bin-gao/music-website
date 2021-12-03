<h1 align="center">music-website</h1>

<br/>

<p align="center">
  <a href=""><img alt="license" src="https://img.shields.io/github/license/Yin-Hongwei/music-website?style=flat-square"></a>
</p>



## 项目说明

本音乐网站的客户端和管理端使用 **VUE** 框架来实现，服务端使用 **Spring Boot + MyBatis** 来实现，数据库使用了 **MySQL**。实现思路可以看[这里](https://yin-hongwei.github.io/2019/03/04/music/#more)；项目启动方法看文章末尾。

<br/>

## 项目预览

> 前台截图预览

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec0a2vd9j31c00u0n4z.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec0qtdxrj31c00u07wj.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec19x0e6j31c00u0npe.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec1nmbt4j31c00u0hcf.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec1yc0gkj31c00u0kjm.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec29vvdtj31c00u0nok.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec2ixqk1j31c00u0qf8.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec31i06gj31c00u0wtw.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec3ozxt9j31c00u0qbv.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1geec41r7onj31c00u047y.jpg)<br/>

> 后台截图预览

![](https://tva1.sinaimg.cn/large/006tNbRwly1g9hhhu4n7tj31c00u04qq.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1ghrnrvgflvj31c00u0jzh.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1ghrns4ycpkj31c00u0qjl.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1ghrnsfearcj31c00u0axt.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1ghrnsq6s3sj31c00u0tmu.jpg)<br/>

![](https://tva1.sinaimg.cn/large/007S8ZIlly1ghrnszq403j31c00u07nq.jpg)<br/>

## 项目功能

- 音乐播放
- 用户登录注册
- 用户信息编辑、头像修改
- 歌曲、歌单搜索
- 歌单打分
- 歌单、歌曲评论
- 歌单列表、歌手列表分页显示
- 歌词同步显示
- 音乐收藏、下载、拖动控制、音量控制
- 后台对用户、歌曲、歌手、歌单信息的管理

<br/>

## 技术栈

### 后端

**SpringBoot + MyBatis**

### 前端

**Vue + Vue-Router + Vuex + Axios +  ElementUI**

<br/>

## 开发环境

JDK： jdk-8u141

mysql：mysql-5.7.21-1-macos10.13-x86_64

node：v12.4.0

IDE：IntelliJ IDEA 2018、VSCode

<br/>

## 下载运行

#### 1、下载项目到本地

```bash
git clone https://github.com/Yin-Hongwei/music-website.git
```

#### 2、下载数据库中记录的资源

去【链接: https://pan.baidu.com/s/1Qv0ohAIPeTthPK_CDwpfWg 提取码: gwa4 】下载网站依赖的歌曲及图片，将 data 夹里的文件放到 music-server 文件夹下。

> 注意：资源整理了一下，按照下面的截图存放。

<img src="https://tva1.sinaimg.cn/large/008i3skNly1gsk65seqd8j30y00ocjt4.jpg" height="200px"/>

#### 3、修改配置文件
1）创建数据库
将 `music-website/music-server/sql` 文件夹中的 `tp_music.sql` 文件导入数据库。

2）修改用户名密码
修改 `music-website/music-server/src/main/resources/application.properties` 文件里的 `spring.datasource.username` 和 `spring.datasource.password`；

3）修改资源路径

修改 `music-server/src/main/java/com/example/yin/constant/Constants.java` 文件中的 `RESOURCE_PATH`，**否则资源加载不了**。

![](https://tva1.sinaimg.cn/large/008i3skNly1gske6w6kk8j33aq0u0wn2.jpg)

#### 4、启动项目

- **启动管理端**：进入 music-server 文件夹，运行下面命令启动服务器

```js
// 方法一
./mvnw spring-boot:run

// 方法二
mvn spring-boot:run // 前提装了 maven
```

- **启动客户端**：进入 music-client 目录，运行下面命令

```js
npm install // 安装依赖

npm run dev // 启动前台项目
```

- **启动管理端**：进入 music-manage 目录，运行下面命令

```js
npm install // 安装依赖

npm run dev // 启动后台管理项目
```

<br/>



