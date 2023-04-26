<template>
    <div class="pager-contianer" v-if="this.pageNumber > 1">
        <a @click="handleClick(1)" :class="{ disabled: this.current === 1 }">首页</a>
        <a @click="handleClick(current - 1)" :class="{ disabled: this.current === 1 }">上一页</a>

        <a @click="handleClick(n)" v-for="(n, i) in pagesList" :key="i" :class="{ active: current === n }">{{ n }}</a>

        <a @click="handleClick(current + 1)" :class="{ disabled: this.current === pageNumber }">下一页</a>
        <a @click="handleClick(pageNumber)" :class="{ disabled: this.current === pageNumber }">尾页</a>
    </div>
</template>

<script>
export default {
    methods: {
        handleClick(newPage) {
            if (newPage < 1) {
                newPage = 1
            }
            if (newPage > this.pageNumber) {
                newPage = this.pageNumber
            }
            if (newPage === this.current) {
                return;
            }
            this.$emit('update:current', newPage, "hello", "22")
        }
    },
    props: {
        current: {
            type: Number,
            default: 1
        },
        limit: {
            type: Number,
            default: 10
        },
        total: {
            type: Number,
            default: 0
        },
        visibleNumber: {
            type: Number,
            default: 10
        },
    },
    computed: {
        pageNumber() {
            return Math.ceil(this.total / this.limit)
        },
        maxPages() {
            let max = this.minPages + this.visibleNumber - 1
            if (max > this.pageNumber) {
                max = this.pageNumber;
            }
            return max;
        },
        minPages() {
            let min = this.current - Math.floor(this.visibleNumber / 2)
            if (min < 1) {
                min = 1;
            }
            return min;
        },
        pagesList() {
            let list = [];
            for (let i = this.minPages; i < this.maxPages; i++) {
                list.push(i)
            }
            return list
        },
    },


}
</script>

<style lang="less" scoped>
@import "~@/styles/var.less";

.pager-contianer {
    display: flex;
    justify-content: center;
    margin: 10px auto;

    a {
        color: @primary;
        margin: 0 6px;
        cursor: pointer;

        &.disabled {
            color: @lightWords;
            cursor: not-allowed;
        }

        &.active {
            color: @active;
            font-weight: bold;
        }
    }

}
</style>