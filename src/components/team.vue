<template>
	<div class="m-content">
		<h1>开发团队</h1>
		<el-container>
			<ul class="m-about-team">
				<li v-for="i in user" :key="i.uuid" class="infinite-list-item">
					<p>{{ i.name }}</p>
					<p>负责：{{ i.res }}</p>
					<p>UUID：{{ i.uuid }}</p>
					<p>邮箱：{{ i.emall }}</p>
				</li>
			</ul>
		</el-container>
		<h2>管理团队</h2>
		<el-container>
			<ul class="m-about-team">
				<li v-for="i in user" :key="i.uuid" class="infinite-list-item">
					<p>{{ i.name }}</p>
					<p>负责：{{ i.res }}</p>
					<p>UUID：{{ i.uuid }}</p>
					<p>邮箱：{{ i.emall }}</p>
				</li>
			</ul>
		</el-container>
	</div>
</template>

<script>
export default {
	name: 'team',
	props: [],

	data: function() {
		const item = {
			uuid: 1,
			name: '李先生',
			res: '活动策划',
			emall: 'li@jx3box.com',
		}
		return {
			user: Array(20).fill(item),
		}
	},
	computed: {},
	methods: {},
	mounted: function() {},
	components: {},
}
</script>

<style lang="less">
@import '../assets/css/team.less';
.m-content {
	min-width: 1000px;
	max-height: 700px;
	overflow-x: hidden;
	overflow-y: scroll;
}
</style>
<style lang="less" scoped>
.m-content {
 
	h2 {
		text-align: center;
	}
	.m-about-team {
		display: flex;
		justify-content: space-around;
		flex-wrap: wrap;
		width: 100%;
		list-style: none;
		li {
			font-size: 14px;
			color: #555;
			line-height: 40px;
			border: 1px solid #ddd;
			width: 20%;
			padding: 10px 1%;
			margin: 10px 20px;
			p {
				padding: 0;
				margin: 0;
			}
		}
	}
}
</style>
