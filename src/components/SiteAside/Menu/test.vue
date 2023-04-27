<template>
    <div class="test-container">
        <Menu></Menu>
    </div>
</template>

<script>
import Menu from "./"
export default {
    components: {
        Menu,
    },

}
</script>

<style lang="less" scoped>
.test-container {
    width: 400px;
    height: 500px;
    margin: 30px auto;
    background-color: black;
}
</style>