<template>
	<div class="m-content">
		<h1>联系合作</h1>
		<div class="m-about-contact">
			<div>
				<p>QQ</p>
				<p>
					<a
						href="http://wpa.qq.com/msgrd?v=3&amp;uin=17229398&amp;site=qq&amp;menu=yes"
						target="_blank"
						rel="noopener noreferrer"
						><img
							title="点击这里给我发消息"
							src="http://wpa.qq.com/pa?p=2:17229398:51"
							alt="点击这里给我发消息"
							border="0"
					/></a>
				</p>
			</div>
			<div>
				<p>
					邮箱
				</p>
				<p>rx6@qq.com</p>
			</div>
		</div>

		<h2>合作伙伴</h2>
		<div class="m-about-partner">
			<el-row>
				<el-col :span="8" v-for="item in 2" :key="item">
					<el-card>
						<img
							src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"
							class="img"
						/>
						<a class="title" href="">胖叔叔配装器</a>
					</el-card>
				</el-col>
			</el-row>
		</div>

		<h2>鸣谢</h2>
		<div class="m-about-thanks">
			<a href=""><img src="http://game.gtimg.cn/images/game/web201910/images/logo.png"/></a>
		</div>
	</div>
</template>

<script>
export default {
	name: 'thanks',
	props: [],
	data: function() {
		return {}
	},
	computed: {},
	methods: {},
	mounted: function() {},
	components: {},
}
</script>

<style lang="less">
@import '../assets/css/thanks.less';
.m-content {
	min-width: 1000px;
	max-height: 700px;
	overflow-x: hidden;
	overflow-y: scroll;
}
</style>
<style lang="less" scoped>
h2 {
	padding-top: 30px;
}
.m-about-contact {
	max-width: 600px;
	margin: 0 auto;
	display: flex;
	border: 1px solid #ddd;
	padding: 10px 20px;
	text-align: center;
	justify-content: space-around;
}
.m-about-partner {
	text-align: center;
	.img {
		width: 380px;
		height: 240px;
	}
	.title {
		display: block;
		color: #555;
		line-height: 40px;
		font-weight: bold;
		height: 40px;
	}
}
.m-about-thanks {
	display: flex;
	justify-content: flex-start;
	flex-wrap: wrap;
	a {
		display: block;
		position: relative;
		background: #000;
		width: 200px;
		height: 60px;
		margin: 0 10px 20px 0;
		img {
			position: absolute;
			left: 0;
			top: 0;
			bottom: 0;
			right: 0;
			width: 100%;
			height: 100%;
		}
	}
}
</style>
