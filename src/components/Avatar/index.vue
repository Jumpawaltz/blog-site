<template>
    <div>
        <img class="avatar-container" :src="url" :style="{ width: size + `px`, height: size + `px` }">
    </div>
</template>

<script>
//  预编译， 打包没有模板系统，cli会将模板转化成渲染函数，从而减少打包文件大小 
export default {
    data() {
        return {
        }
    },
    props: {
        url: {
            require: true,
            type: String
        },
        size: {
            require: true,
            type: Number
        },

    }
}
</script>

<style lang="less" scoped>
.avatar-container {
    border-radius: 50%;
    display: block;
    object-fit: cover;
}
</style>