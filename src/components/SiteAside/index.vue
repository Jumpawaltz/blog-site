<template>
    <div class="site-aside-container">
        <div class="avatar-wrap">
            <Avatar :size="150"
                url="https://img.freepik.com/free-photo/portrait-young-adult-wearing-hoodie-mockup_23-2149296306.jpg?w=1060&t=st=1682604678~exp=1682605278~hmac=79a62b48d0d0a5ec48ff0eadd66c9a37392ccaffe1c3c677e4ad16a0e8af37b4">
            </Avatar>
            <h2 class="title">zy的blog</h2>
        </div>
        <Menu></Menu>
        <Contact />
    </div>
</template>

<script>
import Avatar from "@/components/Avatar";
import Menu from "./Menu";
import Contact from "./Contact";
export default {
    components: {
        Avatar,
        Menu,
        Contact
    },

}
</script>

<style lang="less" scoped>
@import "~@/styles/global.less";
@import "~@/styles/var.less";

.site-aside-container {
    width: 100%;
    height: 100%;
    overflow-x: hidden;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    background-color: @dark ;
    padding: 20px 0;

    .avatar-wrap {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        color: #fff;
        .title {
            margin-top: 10px;
        }
    }
}
</style>