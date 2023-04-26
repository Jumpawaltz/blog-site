<template>
    <div class="test-container">
        <div class="item" v-for="i in types" :key=i>
            <Icon :type="i"></Icon>
            <label>{{ i }}</label>
        </div>
    </div>
</template>

<script>
import Icon, { types } from "./index.vue"
export default {
    data() {
        return {
            types
        }
    },
    components: {
        Icon
    },

}
</script>

<style lang="less" scoped>
.test-container {
    font-size: 1rem;
    display: flex;
    width: 800px;
    margin: 20px auto;
    flex-flow: row wrap;

    .item {
        padding: 10px;
        display: flex;
        text-align: center;
        flex-direction: column;
        margin: 0 8px;
    }
}
</style>