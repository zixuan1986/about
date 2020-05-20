<template>
	<div id="app">
		<Header />
		<div class="c-container">
			<div class="c-nav">
				<ul class="ul">
					<li v-for="(item, index) in navs" :key="index" :class="{ atv: atv == index }" @click="atv = index">
						{{ item }}
					</li>
				</ul>
			</div>
			<div class="c-box">
				<div class="box" v-show="atv == 0"><about /></div>
				<div class="box" v-show="atv == 1"><team /></div>
				<div class="box" v-show="atv == 2"><thanks /></div>
				<div class="box" v-show="atv == 3"><privacy /></div>
				<div class="box" v-show="atv == 4"><licence /></div>
				<div class="box" v-show="atv == 5"><treaty /></div>
			</div>
		</div>
	</div>
</template>

<script>
import about from '@/components/about.vue'
import team from '@/components/team.vue'
import thanks from '@/components/thanks.vue'
import privacy from '@/components/privacy.vue'
import licence from '@/components/licence.vue'
import treaty from '@/components/treaty.vue'

export default {

	name: 'App',
	props: [],
	data: function() {
		return {
			tabPosition: 'left',
			navs: ['关于我们', '加入我们', '合作伙伴', '隐私政策', '用户协议', '创作公约'],
			atv: 0,
		}
	},
	methods: {},
	computed: {},

	mounted: function() {},
	components: {
		about,
		team,
		thanks,
		privacy,
		licence,
		treaty,
	},
}

</script>

<style lang="less">
@import './assets/css/common.less';
</style>
<style lang="less" scoped>
@width: 1000px;
@nav: #4d4d4f;
@con: #fafafa;
.c-container {
	position: relative;
}
.c-nav {
	position: relative;
	height: 100%;
	ul {
		width: 260px;
		position: absolute;
		z-index: 1;
		background: url(https://console.cnyixun.com/img/common/jx3box_white.svg) no-repeat 0 20px @nav;
		padding: 300px 0 180px 0;
		border-radius: 10px;
		border-top-left-radius: 0;
		border-bottom-left-radius: 0;
		list-style-type: none;
		.atv + li {
			border-top: 0;
		}
		li {
			width: 200px;
			margin: 0 auto;
			line-height: 50px;
			cursor: pointer;
			color: #f9f9f9;
			text-indent: 66px;
			border-top: 1px solid #ddd;
			&.atv {
				color: #fff;
				font-weight: bold;
				width: 320px;
				text-indent: 96px;
				border-bottom: 1px solid #ddd;
				background: @nav;
				border-top-right-radius: 5px;
				border-bottom-right-radius: 5px;
				background: url(https://console.cnyixun.com/img/footer/logo2.svg) no-repeat 275px center @nav;
				background-size: 24px;
			}
			&:last-child {
				border-bottom: 1px solid #ddd;
			}
		}
	}
}
.c-box {
	position: absolute;
	background: @con;
	width: 100%;
	min-height: 700px;
	top: 100px;
	bottom: 100px;
	border: 1px solid #ddd;
	border-right: 0;
	border-left: 0;
	.box {
		padding: 0 10px 0 360px;
		overflow: hidden;
		min-width: 1360px;
		max-height: 700px;
	}
}
</style>
