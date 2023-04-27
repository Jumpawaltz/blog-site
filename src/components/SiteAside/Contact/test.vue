<template>
    <div class="test-container">
        <Contact />
    </div>
</template>

<script>
import Contact from "./";
export default {
    components: {
        Contact,
    },

}
</script>

<style lang="less" scoped>
.test-container {
    width: 400px;
    height: 800px;
    background-color: black;
    border: 1px solid red;
}
</style>