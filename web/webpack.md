## webpack

#### 2017-9-13

**第一节 什么是webpack**

webpack被开发出来，其根本原因是web服务在其设计之初没有考虑到其升级换代的可能性，导致了许多的***坑*** 。而如今为了能够实现更高效的web开发，发明了踩坑神器webpack。

举一个简单的例子，在js代码中，有一点十分的坑，那就是对于浏览器而言，它无法实现js文件之间的共享和传输，这导致全局变量的大量运用，使得代码的可扩展性和安全性下降。后端的方式写代码，借助node可以运行在操作系统之上，然后再由webpack转换成web可以阅读的方式，从而实现了文件数据的传输和共享。

具体如下：在b.js中定义的变量 通过 module.export(在node中一切都是module){val:val}，导出，再到a.js中使用require().val的方式运用，从而使得数据在js文件之间方便地交换。

**第二节 安装和配置**

如果在全局下安装webpack可能出现版本移植的问题，所以在项目目录下用npm init之后，采用-D选项--save-dev方式在package.json中建立版本号。

配置webpack是一项艰巨的任务。首先使用的是一个漫长的命令行简化到package.json中的script字段中设置一个命令，如"pack" : "././"，然后可以使用npm run pack的方式直接执行命令。但是对于多命令的情况，就需要借助webpack.config.js文件进行配置。其主要的参数是entry和output。

```javascript
//module.exports将会作为webpack命令的配置参数
module.exports = {
    entry: './a',
  	output:{
    	filename: 'pack.js',
    	path: __dirname //解释为当前文件所在的目录名
}
}
```

**第三节 entry和output**

具体而言，对于有多页面的，多打包的项目，可以在配置中，对每一页需要的js进行配置和打包。在各自的js中，可以采用node的写法，也可以采用es6的写法。一个最简单的实现我会在今晚回来以后用20分钟的时间模仿着测试一下。