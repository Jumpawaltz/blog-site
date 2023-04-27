<template>
    <div class="empty-container">
        <Icon :type="type"></Icon>
        <p>{{ text }}</p>
    </div>
</template>

<script>
import Icon from "../Icon"
export default {
    data() {
        return {
            type: "empty"
        }
    },
    props: {
        text: {
            type: String,
            default: "无数据"
        },
    },
    components: {
        Icon,
    },
}
</script>

<style lang="less" scoped>
@import "~@/styles/var.less";
@import "~@/styles/mixin.less";

.empty-container {
    .self-center();
    color: @gray ;
    text-align: center;

    .icon-container {
        font-size: 72px;
    }
}
</style>