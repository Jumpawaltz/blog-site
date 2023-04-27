<template>
    <div class="menu-container">
        <a :href="item.name.toLocaleLowerCase()" v-for="item in items" :key="item.name"
            :class="{ selected: isSelected(item) }">
            <Icon :type="item.icon" />
            <span>{{ item.title }}</span>
        </a>

    </div>
</template>

<script>
import Icon from "@/components/Icon"
export default {
    data() {
        return {
            items: [
                {
                    name: "Home",
                    title: "首页",
                    icon: "home",
                },
                {
                    name: "Blog",
                    title: "文章",
                    icon: "blog",
                    starWith: true,
                },
                {
                    name: "About",
                    title: "关于我",
                    icon: "about",
                },
                {
                    name: "Project",
                    title: "项目&效果",
                    icon: "code",
                },
                {
                    name: "Message",
                    title: "留言板",
                    icon: "chat",
                },
            ],
        }
    },
    components: {
        Icon,
    },
    methods: {
        isSelected(item) {
            const path = "/" + item.name.toLocaleLowerCase();
            const curPathname = location.pathname.toLocaleLowerCase()
            if (item.starWith) {
                return curPathname.startsWith(path)
            }
            return curPathname === path
        }
    }

}
</script>

<style lang="less" scoped>
@import "~@/styles/global.less";
@import "~@/styles/var.less";

.menu-container {
    width: 100%;
    display: flex;
    flex-flow: column;
    color: @gray;
    overflow: hidden;
    margin: 24px 0;

    a {
        display: block;
        height: 45px;
        padding: 0 50px;
        line-height: 45px;

        .icon-container {
            margin-right: 12px;
        }

        &.selected {
            background-color: darken(@words, 3%);
        }

        &:hover {
            color: white;
        }
    }
}
</style>