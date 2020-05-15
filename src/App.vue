<template>
    <div id="app">
        <Header></Header>
        <Breadcrumb name="频道名称" slug="slug" root="/slug" publishEnable="true">
            <img slot="logo" svg-inline src="./assets/img/logo.svg" />
            <!-- <Info /> -->
        </Breadcrumb>
        <LeftSidebar>
            <!-- <Nav /> -->
        </LeftSidebar>
        <Main :withoutRight="false">
            primary content
            <!-- <Comment post-id="100"/> -->
            <RightSidebar>
                <!-- <Extend/> -->
            </RightSidebar>
            <Footer></Footer>
        </Main>
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
        // about,
        // team,
        // thanks,
        // privacy,
        // licence,
        // treaty
    },
};
</script>

<style lang="less">
    @import './assets/css/common.less';
</style>