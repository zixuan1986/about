<template>
    <div id="app">
        <Header />
        <div class="c-container">
            <el-tabs :tab-position="tabPosition">
                <el-tab-pane label="关于我们">
                    <about/>
                </el-tab-pane>
                <el-tab-pane label="加入我们">
                    <team/>
                </el-tab-pane>
                <el-tab-pane label="合作伙伴">
                    <thanks/>
                </el-tab-pane>
                <el-tab-pane label="隐私政策">
                    <privacy/>
                </el-tab-pane>
                <el-tab-pane label="用户协议">
                    <licence/>
                </el-tab-pane>
                <el-tab-pane label="创作公约">
                    <treaty/>
                </el-tab-pane>
            </el-tabs>
        </div>
    </div>
</template>

<script>
import about from "@/components/about.vue";
import team from "@/components/team.vue";
import thanks from "@/components/thanks.vue";
import privacy from "@/components/privacy.vue";
import licence from "@/components/licence.vue";
import treaty from "@/components/treaty.vue";

export default {
    name: "App",
    props: [],
    data: function () {
        return {
            tabPosition : 'top'
        };
    },
    computed: {},
    methods: {},
    mounted: function () {},
    components: {
        about,
        team,
        thanks,
        privacy,
        licence,
        treaty
    },
};
</script>

<style lang="less">
    @import './assets/css/common.less';
</style>