<template>
    <div class="test-container">
        <ImageLoader :src="src" :placeHolder="pleaceHolder" @load="handle"></ImageLoader>
    </div>
</template>

<script>
import ImageLoader from "./"
export default {
    data() {
        return {
            src: "https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?fit=crop&crop=entropy&w=3456&h=2304",
            pleaceHolder: "https://images.pexels.com/photos/33109/fall-autumn-red-season.jpg?w=100"
        }
    },
    components: {
        ImageLoader,
    },
    methods: {
        handle() {
            console.log("img load 完成");
        }
    },

}
</script>

<style lang="less" scoped>
.test-container {
    width: 400px;
    height: 200px;
    margin: 20px auto;
    border: 1px solid #000;
}
</style>