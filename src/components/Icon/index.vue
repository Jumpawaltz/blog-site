<template>
    <i :class="MapClass" class="iconfont icon-container"></i>
</template>

<script>
const classMap = {
    home: "iconzhuye",
    success: "iconzhengque",
    error: "iconcuowu",
    close: "iconguanbi",
    warn: "iconjinggao",
    info: "iconxinxi",
    blog: "iconblog",
    code: "iconcode",
    about: "iconset_about_hov",
    weixin: "iconweixin",
    mail: "iconemail",
    github: "icongithub",
    qq: "iconsign_qq",
    arrowUp: "iconiconfonticonfonti2copy",
    arrowDown: "iconiconfonticonfonti2",
    empty: "iconempty",
    chat: "iconliuyan",
};
export const types = Object.keys(classMap)
export default {
    data() {
        return {
            classMap
        }
    },
    computed: {
        MapClass() {
            return classMap[this.type]
        }
    },
    props: {
        type: {
            type: String,
            require: true,
        }
    }

}
</script>

<style  scoped>
@import "//at.alicdn.com/t/font_2164449_nalfgtq7il.css";

.iconfont {
    font-size: 1rem;
    color: red;
    color: inherit;
    font-size: inherit;
}
</style>