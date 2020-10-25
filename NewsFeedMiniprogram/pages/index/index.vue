<template>
	<view style="flex-wrap:wrap;">
	<navigator class="news-list" :url="'../info/info?newsid='+item.article_id" v-for="(item, index) in news">
		<image src="https://dss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=16207085,969658569&fm=26&gp=0.jpg" mode="widthFix"></image>
		<view class="news-title">
		{{item.article_title}}
		</view>
	</navigator>
	</view>
</template>

<script>
	var _self;
	export default {
		data() {
		return{ 
         news: [],
		 }
		},
		onLoad() {
			_self = this;
        this.getNews();
		},
		methods: {
          getNews: function(){
			  uni.request({
				url:"http://0.0.0.0:7300/mock/5f8e78c36265d39867d69dd0/news",
				success:function(res){
					console.log(res);
				_self.news = res.data.data;
					
				}
			  })
		  }
		}
	}
</script>

<style>
view{width: 100%;}
.news-list{
	display:flex;
	width: 94%;
	padding: 10upx 3%;
	flex-wrap:nowrap;
	margin:12upx 0;
	}
.news-list image{
	width: 200upx;
	margin-right: 12upx;
	flex-shrink: 0;
	}
.news-title{
	width:100%;
	height:auto;
	font-size:28upx;
	}

</style>
