<template>
    <ul class="contact-container">
        <li>
            <a href="" class="">
                <Icon type="github" />
                <span class="text">github2423</span>
            </a>
        </li>
        <li>
            <a href="mailto:zy.me@outlook.com" class="">
                <Icon type="mail" />
                <span class="text">zy.me@outlook.com</span>
            </a>
        </li>
        <li>
            <a href="" class="">
                <Icon type="weixin" />
                <span class="text">weixin</span>
            </a>
            <div class="pop">
                <img src="http://www.duyiedu.com/source/img/%E5%85%AC%E4%BC%97%E5%8F%B7%E4%BA%8C%E7%BB%B4%E7%A0%81.png"
                    alt="" />
            </div>
        </li>
        <li>
            <a class=""
                href="tencent://message/?Menu=yes&uin=1347753242&Service=300&sigT=45a1e5847943b64c6ff3990f8a9e644d2b31356cb0b4ac6b24663a3c8dd0f8aa12a595b1714f9d45">
                <Icon type="qq" />
                <span class="text">qq234523452345234</span>
            </a>
            <div class="pop">
                <img src="http://www.duyiedu.com/source/img/%E5%85%AC%E4%BC%97%E5%8F%B7%E4%BA%8C%E7%BB%B4%E7%A0%81.png"
                    alt="" />
            </div>
        </li>
    </ul>
</template>

<script>
import Icon from "@/components/Icon"
export default {
    components: {
        Icon,
    },

}
</script>

<style lang="less" scoped>
@import "~@/styles/var.less";
@import "~@/styles/global.less";

.contact-container {
    width: 100%;
    padding: 30px;
    background-color: transparent;
    display: flex;
    flex-direction: column;

    @itemHeight : 30px;

    li {
        height: 30px;
        position: relative;
        margin: 8px 3px;

        a {
            display: flex;
            align-items: center;
            cursor: pointer;
            color: @gray;

            &:hover {
                color: primary;
            }

            .icon-container {
                font-size: 32px;
                margin-right: 12px;
            }
        }

        .pop {
            position: absolute;
            bottom: @itemHeight+8px;
            left: 0;
            padding: 10px;
            background-color: #fff;
            border-radius: 5px;
            transform: scaleY(0);
            transform-origin: bottom center;
            transition: 0.4s;

            img {
                width: 150px;
                height: 150px;
                border: 1px solid #000;
            }

            &::before {
                content: "";
                position: absolute;
                left: 50%;
                bottom: -4px;
                transform: translateX(-50%) rotate(45deg);
                height: 0;
                width: 0;
                border: 8px solid #fff;
            }
        }

        &:hover .pop {
            transform: scaleY(1);
        }
    }
}
</style>