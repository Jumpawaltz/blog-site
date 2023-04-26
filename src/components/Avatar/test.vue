<template>
    <div>
        <Avatar :url="url" :size="size"></Avatar>
        {{ url }}
    </div>
</template>

<script>
import Avatar from './index.vue'
export default {
    data() {
        return {
            size: 400,
            url: "https://pic1.zhimg.com/80/v2-1c8b6ff9598bd00b2fb9d6d5fb6d5d38_1440w.webp?source=1940ef5c"
        }
    },
    components: {
        Avatar
    },

}
</script>

<style lang="scss" scoped></style>