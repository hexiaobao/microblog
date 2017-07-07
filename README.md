# microblog
based on node.js 


基于node.js、exppress框架和mongoDB数据库的微博的网站开发项目

一、搭建node.js项目的基本框架

首先使用espresso框架创建项目的基本目录，在这之前先要安装noode.js,安装步骤及配置步骤如下:

1、安装node.js，在node的官网上下载最新版的node.js安装,下载网址https://nodejs.org/en/download/；

2、配置关于node.js的环境变量，将node.js的bin目录的路径添加到path中在命令行输入node -v和npm -v检测node.js是否安装成功，出现版本号则表示安装成功！

3、修改node.js的全局目录，在命令行输入npm config set prefix "xxx" , //xxx 代表目录路径

4、修改node.js的缓存目录，在命令行输入npm config set cache "xxx" , //xxx代表缓存目录路径 其次是安装MongoliaDB数据库及其相对应的图形化界面robomongo

1、在mongoDB官网上下载安装包，按照安装向导安装

2、在安装目录下面新建文件夹为db,用来存放数据

3、在命令行输入mongod.exe --dbpath xxx\db //xxx代表你安装mongoDB的目录

4、在robomongo官网上下载安装robomongo，并且创建与mongoDB数据库的连接，端口号默认为27017，默认地址为localhost 最后安装express框架

1、在全局模式下安装，不然在测试过程中会出现express不是内部或者外部命令的错误，在命令行中输入npm insiall -g express

2、由于express4.x 版本将命令工具分离出来，还需要安装express-generator,在命令行中输入npm install -g express-generator

3、检测express 是否安装成功，在命令行输入express -V,(注意V是大写的哦)，如果出现版本号则说明安装成功 接下来我们就要开始我们的node的开发之旅

1、创建项目，名称为microblog

2、命令行中输入：cd microblog

3、命令行中输入：express microblog,用express框架生成项目的目录

4、命令行中输入：npm install,npm start来启动项目 5、在浏览器的地址栏中输入localhost:3000,若出现express，welcome to express ,则表示项目框架搭建完成

二、搭建完成，接下来编写相关代码

首先在views下面的layout.jade中编写有关整个项目中的公共部分，说白了就是写一个模板，然后在其他的jade中用extends layout去引用这个模板，到目前为止，启 动整个项目，你就可以看到整个项目的大体样子了。
