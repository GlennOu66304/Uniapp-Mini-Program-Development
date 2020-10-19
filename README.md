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

## Run the project:     

### 1.download the projet:  
1.just keep the VPN mode and data, then right click the destination file;  
2.then it will download and have the project file;   

### 2.How to run the local project into the wechat dev tool:   
1.You need to import the project into the HbuilderX;  
2.Run this app into the wechat tab; (HbuilderX)  
3.compile the projec to see more content;(Wechat developer tool)  
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

## 小程序，app调试环境配置  
[小程序调试](https://juejin.im/book/6844733817438076936/section/6844733817547128839)   
[如何获取小程序的appid](https://zhuanlan.zhihu.com/p/61511399)   
[小程序链接](https://mp.weixin.qq.com/wxamp/devprofile/get_profile?token=1113910923&lang=zh_CN) 
[如何安装配置手机模拟器](https://ask.dcloud.net.cn/article/151)   

## Lerninin resource:  
[Uniapp 从入门到进阶](https://juejin.im/book/6844733817438076936)  
[Dcloun社区](https://ask.dcloud.net.cn/explore/)  
[uniapp-music-code source code](https://github.com/front-end-class/uniapp-music-code)  
[官方免费项目：新冠病毒，IT系统总汇]（https://dcloud.io/ncp.html）