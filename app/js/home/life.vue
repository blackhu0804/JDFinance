<template lang="html">
    <Panel title="生活服务" :class="$style.panel">
        <ul :class="$style.content">
            <li :class="$style.item" v-for="item in items" :key="item.title">
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
                src: "//img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90",
                title: "旅游",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90",
                title: "医美",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88",
                title: "房抵贷",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90",
                title: "驾校",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t14896/125/1435676873/3668/a8b392f7/5a4f26edN6cdfda66.png?width=88&height=88",
                title: "分期用",
            }],
        }
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        .content {
            @include flex(row);
            padding-bottom: 40px;
            -webkit-box-sizing: border-box;
            -moz-box-sizing: border-box;
            box-sizing: border-box;
            justify-content: space-around;
            text-align: center;
            a {
                text-decoration: none;
            }
            p {
                font-size: 26px;
                text-align: center;
                color: #666;
                margin-top: 12px;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
            }
        }
    }
</style>
