<template lang="html">
    <Panel title="便利生活" :class="$style.panel">
        <h3>便利生活</h3>
        <ul :class="$style.nav">
            <li v-for="item in items" :key="item.title">
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
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25093/298/548334833/8788/aa921a45/5b7404a3N1c1aeed4.png?width=90&height=90",
                title: "机票",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22498/165/2150692912/9109/6f2888c0/5b7404aaN77368bad.png?width=90&height=90",
                title: "每日特惠",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22675/60/2122507512/8898/8c1b91c0/5b7404b2N9f01a8a0.png?width=90&height=90",
                title: "领钢镚",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t24247/70/2092785913/8667/86f60d06/5b7404b9Nc12a3479.png?width=90&height=90",
                title: "租车",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25504/251/550721724/8648/ff7cf233/5b7404c0Nb3c19374.png?width=90&height=90",
                title: "电影票",
            }],
        }
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        >h4 {
            display: none;
        }
        .nav {
            @include flex(row);
            justify-content: space-around;
            flex-wrap: nowrap;
            li {
                text-align: center;
                margin: 38px 19px 0;
                a {
                    text-decoration: none;
                    font-size: 22px;
                    color: #333;
                    p {
                        margin: 18px 0 48px;
                    }
                }
            }
        }
    }
</style>
