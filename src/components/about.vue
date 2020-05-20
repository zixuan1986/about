<template>
	<div class="m-content">
		<el-carousel height="200px" direction="vertical" :autoplay="true">
			<el-carousel-item v-for="item in 3" :key="item">
				<h3 class="medium">{{ item }}</h3>
			</el-carousel-item>
		</el-carousel>
		<h1>简介</h1>
		<div class="m-about-intro">
			<p>这里是由原超级宏&JX3PVE官方站原班人马打造的全新资料站。</p>
			<p>
				我们不会做和官方推栏重复的内容，旨在服务深度骨灰玩家。如果你觉得好用，欢迎推荐给你的小伙伴。
			</p>
			<p>
				我们的宗旨是，将游戏中较难的部分深度解析，不再让某些利益掌握在小部分人手中，你想知道的，都可以来问，大神会为你解答！
			</p>
		</div>

		<div class="m-box container ">
			<div class="box">
				<h4>官方反馈群</h4>
				<p>2471800</p>
			</div>
			<div class="box">
				<h4>签约作者群</h4>
				<p>978285140</p>
			</div>
			<div class="box">
				<h4>成就讨论群</h4>
				<p>614370825</p>
			</div>
			<div class="box">
				<h4>官方QQ群</h4>
				<p>
					<a
						href="//shang.qq.com/wpa/qunwpa?idkey=572b2fb2d286dda8e49fce1493a17265b9a5d5f062fde9c66180fbc316b90067"
						target="_blank"
						rel="noopener noreferrer"
						><img title="JX3BOX" src="//pub.idqqimg.com/wpa/images/group.png" alt="JX3BOX" border="0"
					/></a>
				</p>
			</div>
			<div class="box">
				<h4>官方邮箱</h4>
				<p>admin@jx3box.com</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'about',
	props: [],
	data: function() {
		return {
			reverse: true,
			activities: [
				{
					content: '活动按期开始',
					timestamp: '2018-04-15',
				},
				{
					content: '通过审核',
					timestamp: '2018-04-13',
				},
				{
					content: '创建成功',
					timestamp: '2018-04-11',
				},
			],
		}
	},
	computed: {},
	methods: {},
	mounted: function() {},
	components: {},
}
</script>

<style lang="less">
@import '../assets/css/about.less';
</style>
<style lang="less" scoped>
.m-content {
	width: calc(100% + 30px);
}
.m-content {
	h1,
	.m-about-intro {
		text-align: center;
	}
	.container {
		display: -webkit-box; /* Chrome 4+, Safari 3.1, iOS Safari 3.2+ */
		display: -moz-box; /* Firefox 17- */
		display: -webkit-flex; /* Chrome 21+, Safari 6.1+, iOS Safari 7+, Opera 15/16 */
		display: -moz-flex; /* Firefox 18+ */
		display: -ms-flexbox; /* IE 10 */
		display: flex; /* Chrome 29+, Firefox 22+, IE 11+, Opera 12.1/17/18, Android 4.4+ */
	}

	.m-box {
		padding-top: 40px;
		justify-content: space-around;
		.box {
			border: 3px double #ddd;
			min-width: 240px;
			text-align: center;
			padding: 10px;
		}
	}
}
</style>
