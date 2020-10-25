# News Feed Miniprogram  
## can not see the color change in the wechat dev tool:
You need to make sure that class not calls in the view:  
```
<view class="news-title">
```
## If you see your red wrap cove the whole page, then you need to go to the app.vue file, and remove the min-height in the page value;  

 ## Bug Fixing:" Errors compiling template:
20:51:22.884   Cannot use v-for on stateful component root element because it renders multiple elements."  

You need to add a root view to cover the navigator
[Cannot use v-for on stateful component root element because it renders multiple elements?](https://stackoverflow.com/questions/44193822/cannot-use-v-for-on-stateful-component-root-element-because-it-renders-multiple/45200570)  
[Cannot use v-for on stateful component root element because it renders multiple elements](https://blog.csdn.net/rj2017211811/article/details/104325983)  

## self is not defined:  
You need to make sure that, there is a space between var and self:  
```
var _self;
```
the location should be above the export
## Bug Fixing:"vue 报错data functions should return an object:"
Simply add the code belolw into the index.vue:
```
data() {
			return{}
		},
```
## if you could not see the image show in the wecht dev:

You need to make sure that you need add : before the src, like the code below:  
```
<image v-if="item.type == 'img'" :src="item.content" style="width:100%;" mode="widthFix"></image>
```
## Learning Resource: 

[uni-app 跨平台应用开发教程](https://ke.qq.com/user/index/index.html#/plan/cid=323825&tid=100384338&term_id=100384338)  
[source code](https://ke.qq.com/course/323825)  
Data JSON source:[News feed JSON](https://github.com/GlennOu66304/Uniapp-Mini-Program-Development/blob/master/News%20feed%20JSON), remove the first title then past the content into the easy mock