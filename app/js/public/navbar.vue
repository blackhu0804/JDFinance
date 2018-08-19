<template lang="html">
    <Panel title="导航条" :class="$style.panel">
        <ul :class="$style.content" >
            <li v-for="(item, index) in items" :key="item.title">
                <router-link :to="{name: item.href}">
                    <img :src="item.src" :alt="item.title">
                    <p>{{ item.title }}</p>
                </router-link>
            </li>
        </ul>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t17587/158/1300523690/1908/eabacaac/5ac4850bNdf876dd8.png?width=60&height=60",
                title: "首页",
            }, {
                href: "makemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t7690/252/3621724688/1715/757a3ca1/59e9d81bN27304850.png?width=60&height=60",
                title: "赚钱",
            }, {
                href: "borrowmoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t18640/141/744623906/1296/82809719/5aa79389N46ec948f.png?width=40&height=40",
                title: "借钱",
            }, {
                href: "savemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t19729/201/1027312338/1395/95cecd48/5ab85d0eN01f81011.png?width=56&height=56",
                title: "省钱",
            }, {
                href: "download",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t10897/141/1894216742/2046/ad0e8dc1/59e9d7feNaa5dd2fd.png?width=60&height=60",
                title: "金融会员",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
    .panel {
        @include panel;
        position: fixed;
        left: 0;
        right: 0;
        bottom: 0;
        height: 100px;
        margin: 0 !important;
        z-index: 101;
        h4 {
            display: none;
        }
        .content {
            @include flex(row);
            justify-content: space-around;
            li {
                text-align: center;
                a {
                    text-decoration: none;
                }
                img {
                    width: 44px;
                    height: 44px;
                    display: inline-block;
                    margin: 12px auto 6px;
                }
                p {
                    font-size: 22px;
                    color: #656565;
                }

            }
        }
    }
</style>

<style lang="scss">
    .router-link-exact-active {
        p {
            color: rgb(70, 104, 255) !important;
        }
    }
</style>
