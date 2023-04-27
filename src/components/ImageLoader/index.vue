<template>
    <div class="ImageLoader-container">
        <img class="placeHolder" v-if="!everyThing" :src="placeHolder" alt="">
        <img class="orgin" :src="this.src" @load="load" :style="{ opacity: orginOpacty, transition: `${duration}ms` }">
    </div>
</template>

<script>
export default {
    data() {
        return {
            everyThing: false,
            isLoad: false
        }
    },
    computed: {
        orginOpacty() {
            return this.isLoad ? 1 : 0
        }
    },
    props: {
        src: {
            type: String,
            require: true
        },
        placeHolder: {
            type: String,
            require: true
        },
        duration: {
            type: Number,
            default: 500
        },
    },
    methods: {
        load() {
            this.isLoad = true
            setTimeout(() => {
                console.log("laod");
                this.everyThing = true
                this.$emit("load")
            }, this.duration);
        }
    },

}
</script>

<style lang="less" scoped>
@import "~@/styles/mixin.less";

.ImageLoader-container {
    width: 100%;
    height: 100%;
    overflow: hidden;
    position: relative;

    .placeHolder {
        filter: blur(2vw)
    }


    img {
        .self-fill();
        object-fit: cover;
    }
}
</style>