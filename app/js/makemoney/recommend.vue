<template lang="html">
    <Panel title="特色推荐" :class="$style.panel">
        <section :class="$style.content">
            <ul>
                <li v-for="item in items" :key="item.title" :class="$style.item">
                    <router-link :to="{ name: item.href }">
                        <img :src="item.src" :alt="item.title">
                        <p :class="$style.title">{{ item.title }}</p>
                        <p :class="$style.price">￥{{ item.price }} <span>起</span></p>
                        <div :class="$style.progress">
                            <div :class="$style.progressInner"/>
                            <span>{{ item.percent }}</span>
                        </div>
                    </router-link>
                </li>
            </ul>
        </section>
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
                href: "makemoney",
                src: "https://img30.360buyimg.com/cf/jfs/t23260/153/2061046931/53522/fa9279f/5b72a2b0Nda227f24.jpg!q70.dpg",
                title: "黑鲨游戏手机CMEL电竞版",
                price: "4499.00",
                percent: "102%",
            }, {
                href: "makemoney",
                src: "https://img30.360buyimg.com/cf/jfs/t25762/241/524109351/30868/be59f03c/5b72cd8fN3361b912.jpg!q70.dpg",
                title: "舍不得放下的马克杯",
                price: "38.00",
                percent: "≥999%",
            }, {
                href: "makemoney",
                src: "https://img30.360buyimg.com/cf/jfs/t20281/109/2360875226/53829/cd6265a0/5b5146e1N1f8aab84.jpg!q70.dpg",
                title: "网易三音云音箱",
                price: "799.00",
                percent: "493%",
            }, {
                href: "makemoney",
                src: "https://img30.360buyimg.com/cf/jfs/t23260/153/2061046931/53522/fa9279f/5b72a2b0Nda227f24.jpg!q70.dpg",
                title: "你试过这么方便的充电方式吗",
                price: "26.00",
                percent: "124%",
            }, {
                href: "makemoney",
                src: "https://img30.360buyimg.com/cf/jfs/t24412/328/1043183669/49189/8ad1d6d0/5b4dbb68N307d0979.jpg!q70.dpg",
                title: "未豆冲牙器 随时洁牙",
                price: "29.00",
                percent: "≥999%",
            }, {
                href: "makemoney",
                src: "https://img30.360buyimg.com/cf/jfs/t24199/150/2081670111/42970/ca626309/5b73e098Ndae30eb2.jpg!q70.dpg",
                title: "GPD 口袋电脑二代",
                price: "3489.00",
                percent: "≥999%",
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
            ul {
                display: flex;
                flex-wrap: wrap;
                li {
                    width: 50%;
                    box-sizing: border-box;
                    border-bottom: 5px solid #f5f5f5;
                    a {
                        text-decoration: none;
                        color: #333;
                    }
                    img {
                        width: 228px;
                        height: 180px;
                        padding: 44px 44px 20px;
                    }
                    p {
                        padding-left: 30px;
                    }
                    .title {
                        margin: 22px 0;
                        overflow: hidden;
                        -ms-text-overflow: ellipsis;
                        text-overflow: ellipsis;
                        white-space: nowrap;
                        font-size: 30px;
                    }
                    .price {
                        color: #ff9a1c;
                        font-size: 28px;
                        font-weight: 700;
                        margin-bottom: 14px;
                        span {
                            color: #999;
                            margin-left: 10px;
                            font-size: 22px;
                        }
                    }
                    .progress {
                        padding-left: 30px;
                        height: 30px;
                        padding-bottom: 26px;
                        .progressInner {
                            width: 179px;
                            margin-top: 10px;
                            height: 10px;
                            border-radius: 5px;
                            background-image: linear-gradient(270deg,#f55 1%,#ff9c31);
                            float: left;
                        }
                        span {
                            margin-left: 6px;
                            font-size: 20px;
                            float: left;
                            line-height: 30px;
                            color: #999;
                        }
                    }
                    &:nth-child(odd) {
                        border-right: 5px solid #f5f5f5;
                    }
                }
            }
        }
    }
</style>
