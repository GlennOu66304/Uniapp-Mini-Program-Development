# Uniapp develop: 
## 1.Bug 'main package source size 2129KB exceed max limit 2MB'fixing:  
1.Put the image into the CDN;   
2. According to the "Subpackage Loading" in the documeatation to fix it:  
[小程序代码上传时报错](https://developers.weixin.qq.com/community/develop/doc/000cce0349468030c42737ebd5b400)  
[源码包超出最大限制](https://developers.weixin.qq.com/community/develop/doc/000426d97d0b40e6ec57c34cf51800)   
[使用分包](https://developers.weixin.qq.com/miniprogram/dev/framework/subpackages/basic.html)  

## 2.Bug 微信开发者工具报错appServiceSDKScriptError? fixing:  
Go to the manifest.json to put the wechat app id, then restart the HBuilder and wechat dev tool, then rerun the project.  
[HX uniapp新建 项目,微信小程序报错，Cannot read property 'forceUpdate' of undefined](https://ask.dcloud.net.cn/question/100352)  
[微信开发者工具报错appServiceSDKScriptError?](https://developers.weixin.qq.com/community/develop/doc/000626a7820dc0e8b18a172605bc00)  
[微信小程序报错：Cannot read property ‘forceUpdate‘ of undefined](https://blog.csdn.net/xiaoma19941027/article/details/107785067)  
[如何获取小程序的appid？](https://zhuanlan.zhihu.com/p/61511399)  
[小程序官方网址](https://mp.weixin.qq.com/wxamp/devprofile/get_profile?token=1113910923&lang=zh_CN)

## 3.Bug fixing 小程序不在以下 request 合法域名列表中问题:  
Simply go to the details and local setting, then select the "Dose not verify valid domain....", then run the project again.   
[微信小程序请求数据报错： 如若已在管理后台更新域名配置，请刷新项目配置后重新编译项目，操作路径：“详情-域名信息”](https://my.oschina.net/u/2423404/blog/3116714)  
[小程序不在以下 request 合法域名列表中问题](https://izhizuo.cn/post/133.html)  
[使用云服务开发小程序，在小程序测试界面发生错误？](https://cloud.tencent.com/developer/ask/24053)  
[网络](https://developers.weixin.qq.com/miniprogram/dev/framework/ability/network.html)  

## 4. HbuilderX:Bug:"文件查找失败：’./pages/index/index.nvue’".  
Just head to the pages.json, then delete the path "./pages/index/index.nvue", then rebuild the pages again(directory), then rerun the project again.  
[uniapp 组件导入文件查找失败](https://cloud.tencent.com/developer/article/1685334)  
[新建页面](https://www.lagou.com/lgeduarticle/41127.html)  

## 5. How to see two files in the two panel in the HBuilderX  
open two files at the same time in the HBuiderX, you could sipmply click a file and open it in the editor, then right click the file choose to open it in the left and right option. it will generate a blank file. then you could drag the deestination file above and right drag to the right area. then click the blank file. 
##6.if you could not see the info page in while you click the test, then you need to check the src in the index.vue page: make sure that it is code below:  
```
<navigator url="../info/info">
```
Resources link:  
[uni app 零基础小白到项目实战（完）](https://www.bilibili.com/video/BV1nb411g79e?p=26)    

6.put the image Link into the miniprogram, make sure the image source is from the Baidu;   
7.编辑器自动换行设置，在Preferencesetting,编辑器设置Here to change.  
[HbuilderX如何设置自动换行](https://jingyan.baidu.com/article/3a2f7c2e5b859766afd61190.html)
## Bug Fixing:"vue 报错data functions should return an object:"  
Simply add the code belolw into the index.vue:  
```
data() {
			return{}
		},
```
[vue 报错data functions should return an object:](https://blog.csdn.net/zhuoganliwanjin/article/details/88331611)  

## Mac搭建easy-mock本地环境:
1.install nodev8.x,: 
[How to install older version of node.js on Windows?](https://stackoverflow.com/questions/33849714/how-to-install-older-version-of-node-js-on-windows/49780887)  

2.node version check:  
```
node-v
``` 
[How do I check my version of Node.js?](https://support.invisionapp.com/hc/en-us/articles/360033641372-How-do-I-check-my-version-of-Node-js-#:~:text=To%20check%20your%20version%20of,line%20will%20display%20the%20Node.)  
2.Install MongoDB Community Edition on macOS:  
```
brew install mongodb-community@4.4
```
[Install MongoDB Community Edition on macOS](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/)  
3.下载 https://fastdl.mongodb.org/osx/mongodb-osx-ssl-x86_64-4.0.4.tgz 并解压  
4.At the same time, you need to follow the guidence to process next.  
5. create a bash file and open it in the Tex file:  
You just need to open a new shell windows, and type the code below in the shell:
```
open -e .bash_profile
```
[How to set .bash_profile, if it does not exist yet. I want to launch sublime from a command line in Mac](https://stackoverflow.com/questions/39037537/how-to-set-bash-profile-if-it-does-not-exist-yet-i-want-to-launch-sublime-fro)  
6.put the content into the Text file and save it  
```
export PATH=/usr/local/mongodb/bin:${PATH}
```
you need to konw that bash profile is under zt, so you need to open a new shell to do that  
[How to create .bash_profile in macOS](https://medium.com/@yash3x/how-to-create-bash-profile-in-macos-sierra-a0e2a42fa4db)  
7. solve the Bug:Read-only file system when attempting mkdir /data/db on Mac  
```
mongod --dbpath=/Users/user/data/db
```
[Read-only file system when attempting mkdir /data/db on Mac](https://stackoverflow.com/questions/58034955/read-only-file-system-when-attempting-mkdir-data-db-on-mac)  
8.Mongo running bug fixing:  
A: try this one first:
```
sudo systemctl enable mongod
```
[Mongodb connection error whenever rebooting server](https://stackoverflow.com/questions/63294890/mongodb-connection-error-whenever-rebooting-server)  
B: the n try this one:  
```
sudo mongod --config /usr/local/etc/mongod.conf
brew services start mongodb-community
```
10.install redis:http://download.redis.io/releases/redis-5.0.2.tar.gz   
11.git install the easy mock:

Main reference:  
[Mac搭建easy-mock本地环境](https://www.jianshu.com/p/8c40dbda6e87)  
[easy-mock](https://github.com/easy-mock/easy-mock/blob/dev/README.zh-CN.md)  
Official doc[快速开始](https://www.easy-mock.com/docs)  
[miniprogram and easy mock:](https://www.cnblogs.com/zyrblog/p/9029746.html)   
## Run the project:     

### 1.download the projet:  
1.just keep the VPN mode and data, then right click the destination file;  
2.then it will download and have the project file;   

### 2.How to run the local project into the wechat dev tool:   
1.You need to import the project into the HbuilderX;   
2. First, you need to go to the mainifest.json to add the wechat appid intot he file, then choose the all options except the location option.  
[小程序调试](https://juejin.im/book/6844733817438076936/section/6844733817547128839)   
3.Run this app into the wechat tab; (HbuilderX)  
4.compile the projec to see more content;(Wechat developer tool)  
[小程序调试](https://juejin.im/book/6844733817438076936/section/6844733817547128839)  

Resource Link:  
[uni-course-实战开发云村页.zip](https://github.com/front-end-class/uniapp-music-code/blob/master/uni-course-%E5%AE%9E%E6%88%98%E5%BC%80%E5%8F%91%E4%BA%91%E6%9D%91%E9%A1%B5.zip)  
[uni-course-router.zip](https://github.com/front-end-class/uniapp-music-code/blob/master/uni-course-router.zip)  
[uniapp-music-code](https://github.com/GlennOu66304/Uniapp-Mini-Program-Development)  
[gitzip](https://kinolien.github.io/gitzip/)  

## Free project download:  
1.Git downloa the project:  
```
git clone https://gitee.com/dcloud/xinguan2020-xuesheng.git(http address) 
```
2.Then follow the above 'Run the project:' solution to run the project:  
3.Project Resource:  
[官方免费项目：新冠病毒，IT系统总汇](https://dcloud.io/ncp.html)

## 工具介绍、新建项目及插件配置
1.You need to install the plugin from the internal HBuilderX  or from the plugin market website:[插件市场](https://ext.dcloud.net.cn/search?q=beautify&cat1=1&cat2=11&orderBy=WeekDownload#)  
2. install the node module: you need to go to the plugin directory, then npm install the package name:  
1. go to the plugin directory:  
```
cd /Applications/HBuilderX.app/Contents/HBuilderX/plugins/

```
2.npm install package:  
```
 npm i js-beautify
```
3.reference link:  
[nodejs插件](https://ask.dcloud.net.cn/article/37379)  
[JS Beautifier](https://www.npmjs.com/package/js-beautify)  
[uni-app 使用npm的问题](https://ask.dcloud.net.cn/question/68943)  


npm version download:  
[How to install older version of node.js on Windows?](https://stackoverflow.com/questions/33849714/how-to-install-older-version-of-node-js-on-windows/49780887)
[easy-mock/README.zh-CN.md](https://github.com/easy-mock/easy-mock/blob/dev/README.zh-CN.md)  

## 小程序，app调试环境配置  
[小程序调试](https://juejin.im/book/6844733817438076936/section/6844733817547128839)   
[如何获取小程序的appid](https://zhuanlan.zhihu.com/p/61511399)   
[小程序链接](https://mp.weixin.qq.com/wxamp/devprofile/get_profile?token=1113910923&lang=zh_CN)   
[如何安装配置手机模拟器](https://ask.dcloud.net.cn/article/151)   

## Lerninin resource:  
[Uniapp 从入门到进阶](https://juejin.im/book/6844733817438076936)  
[uni app 零基础小白到项目实战（完）](https://www.bilibili.com/video/BV1nb411g79e?p=26)  
[2020-web前端-都2020年了你还学习uni-app](https://www.bilibili.com/video/BV1Wa4y1i7r8?p=2)  
[Dcloun社区](https://ask.dcloud.net.cn/explore/)  
[uniapp-music-code source code](https://github.com/front-end-class/uniapp-music-code)  
[官方免费项目：新冠病毒，IT系统总汇]（https://dcloud.io/ncp.html）
[Jshop小程序uniapp前台简约模板](https://gitee.com/hnjihai/uniapp)  
[如何学习 uni-app？](https://yq.aliyun.com/articles/703512)  
[uni-app技术视频](https://blog.csdn.net/qq_26562641/article/details/103164668)  
[uni-app高分开源电影项目源码案例分析，支持一套代码发布小程序、APP平台多个平台(前端入门必看)](https://juejin.im/post/6844904160404455438)  
[uni-app/docs/resource.md](https://github.com/dcloudio/uni-app/blob/master/docs/resource.md)  