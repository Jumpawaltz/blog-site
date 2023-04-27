<template>
    <div class="test-container">
        <Layout>
            <template v-slot:left>
                <div class="left">
                    <SiteAside></SiteAside>
                </div>
            </template>
            <template v-slot:main>
                <div class="mai"></div>
            </template>
            <template v-slot:right>
                <div class="right">right</div>
            </template>
        </Layout>
    </div>
</template>

<script>
import Layout from "./"
import SiteAside from "@/components/SiteAside/"
export default {
    components: {
        Layout,
        SiteAside
    },

}
</script>

<style lang="less" scoped>
.test-container {
    width: 1000px;
    height: 800px;
    border: 1px solid red;
    display: flex;


    .left {
        width: 300px;
        background-color: #666;
        height: 100%;
    }

    .main {
        background-color: green;
        height: 100%;

    }

    .right {
        width: 150px;
        background-color: red;
        height: 100%;
    }
}
</style>