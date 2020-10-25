<template>
	<view style="flex-wrap:wrap;"> 
	<view  style="flex-wrap:wrap;">
		{{news.article_title}}
	</view>
	<view v-for="(item, index) in news.article_content"  style="flex-wrap:wrap;">
		<image v-if="item.type == 'img'" :src="item.content" style="width:100%;" mode="widthFix"></image>
		<text v-if="item.type == 'txt'">
			{{item.content}}			
		</text>
			</view>
			
			</view>
</template>

<script>
	var _self ;
	export default {
     data() {
		return{ 
         news: [],
		 }
		},
		onLoad:function(e){
			_self = this;
			uni.request({
				url:"http://0.0.0.0:7300/mock/5f8e78c36265d39867d69dd0/nesinfo",
				success:function(res){
					_self.news = res.data.data;
					console.log(res);
				}
			})
		}
	}
</script>

<style>

</style>
