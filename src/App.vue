<template>
	<div id="app">
		<Header />
		<div class="c-container">
			<div class="c-box">
				<div class="c-nav">
					<ul>
						<li v-for="(item, index) in navs" :key="index" :class="{ atv: atv == index }" @click="atv = index">
							{{ item }}
						</li>
					</ul>
				</div>

				<div class="c-con">
					<div class="box" v-show="atv == 0"><about /></div>
					<div class="box"  v-show="atv == 1"><team /></div>
					<div class="box"  v-show="atv == 2"><thanks /></div>
					<div class="box"  v-show="atv == 3"><privacy /></div>
					<div class="box"  v-show="atv == 4"><licence /></div>
					<div class="box"  v-show="atv == 5"><treaty /></div>
				</div>
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
	computed: {},
	methods: {},
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
body {
	background: #f6f8fa;
}
</style>
<style lang="less" scoped>
@width: 1000px;
@height: 700px;
@h1: 438px;
@h2: 698px;
@nav: #4d4d4f;
@con: #f0f0f0;
.c-container {
	width: @width;
	padding: 50px;
	margin: 0 auto;
	.c-box {
		height: @height;
		overflow: hidden;
		position: relative;
		background: #fff;
		border: 1px solid #c3c6d5;
		border-radius: 10px;
		.c-nav {
			position: absolute;
			z-index: 1;
			width: 240px;
			height: @h1;
			background: url(https://console.cnyixun.com/img/common/jx3box_white.svg) no-repeat 0 20px @nav;
			left: 1px;
			top: 1px;
			background-size: contain;
			padding: 260px 0 0 0;
			border-top-left-radius: 10px;
			border-bottom-left-radius: 10px;
			ul {
				list-style-type: none;
				border-top: 1px solid #d1d1d1;
				border-bottom: 1px solid #d1d1d1;
				padding: 0;
				.atv + li {
					border-top: 0;
				}
				li {
					width: 200px;
					margin: 0 auto;
					line-height: 50px;
					cursor: pointer;
					color: #f0f0f0;
					text-indent: 66px;
					border-top: 1px solid #ddd;
					&.atv {
						color: #fff;
						font-weight: bold;
						width: 270px;
						text-indent: 86px;
						border-bottom: 1px solid #ddd;
						background: @nav;
						border-top-right-radius: 5px;
						border-bottom-right-radius: 5px;
						background: url(https://console.cnyixun.com/img/footer/logo2.svg) no-repeat 240px center @nav;
						background-size: 24px;
					}
					&:first-child {
						border-top: 0;
                    }
                    &:last-child{
                        border-bottom: 0;
                    }
				}
			}
		}
		.c-con {
			width: 960px;
			margin-left: 20px;
			height: @h2;
			position: absolute;
			background: @con;
			top: 1px;
			right: 1px;
			border-top-right-radius: 10px;
            border-bottom-right-radius: 10px;
            .box{
                padding:0 10px 0 256px;
            }
		}
	}
}
</style>
