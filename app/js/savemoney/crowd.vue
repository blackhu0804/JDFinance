<template lang="html">
    <Panel title="众筹好物" :class="$style.panel">
        <h3>众筹好物</h3>
        <ul>
            <li v-for="item in items" :key="item.title">
                <router-link :to="{name: item.href}">
                    <img :src="item.src" :alt="item.title">
                    <p>{{ item.title }}</p>
                    <p> <em>￥</em>{{ item.price }} <span>起</span></p>
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
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t25591/291/553244587/27582/b0704636/5b73d891N11df935a.jpg!q70.dpg",
                title: "小河豚一壶两杯 小身材随手泡",
                price: "288.00",
            }, {
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t23476/85/2126809896/49799/60e43e87/5b74cc03N50804b53.jpg!q70.dpg",
                title: "鲸鱼造型卫浴套装 点缀生活",
                price: "99.00",
            }, {
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t23404/12/2121182356/30183/fd6e9dc7/5b752114N889d6fbd.jpg!q70.dpg",
                title: "汉能储能发电纸 有光就有电",
                price: "399.00",
            }, {
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t24421/97/2137156254/20865/baae8029/5b752230N90cb0fed.jpg!q70.dpg",
                title: "柏谱自由M3 360便携音响",
                price: "2299.00",
            }, {
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t25828/34/205056918/50666/13c49d5d/5b690f1eN1d0d91ba.jpg!q70.dpg",
                title: "面包沙发全场景随心变",
                price: "399.00",
            }, {
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t24433/17/1886054440/69278/496d5e57/5b6d4f82N6e00dfd4.jpg!q70.dpg",
                title: "长毋相忘 长乐未央手镯",
                price: "359.00",
            }, {
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t24919/126/586286852/28910/26de386b/5b754a14N27dc8fda.jpg!q70.dpg",
                title: "带宝宝穿越时空的安全座椅",
                price: "3380.00",
            }, {
                href: "savemoney",
                src: "//img30.360buyimg.com/cf/jfs/t23938/83/2165711674/25939/ec6f6622/5b75192bNc31fbe7e.jpg!q70.dpg",
                title: "一面湖水 静电HiFi耳机",
                price: "2499.00",
            }],
        }
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        box-sizing: border-box;
        margin-bottom: 120px !important;
        >h4 {
            display: none;
        }
        ul {
            box-sizing: border-box;
            @include flex(row);
            li {
                width: 290px;
                height: 396px;
                background: rgba(0,0,0,.02);
                margin: 0 10px 40px 20px;
                a {
                    text-decoration: none;
                    display: block;
                    text-align: center;
                }
                img {
                    margin: 44px auto 20px;
                    width: 180px;
                    height: 140px;
                    padding-bottom: 40px;
                }
                p:nth-of-type(1) {
                    color: #333;
                    font-size: 28px;
                    height: 40px;
                    line-height: 40px;
                    overflow: hidden;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    margin: 0 24px;
                    font-weight: 700;
                }
                p:nth-of-type(2) {
                    font-weight: 700;
                    font-size: 36px;
                    color: #FF3232;
                    height: 48px;
                    line-height: 48px;
                    em {
                        font-size: 28px;
                    }
                    span {
                        font-size: 20px;
                        color: #999;
                        margin-left: 2px;
                        position: relative;
                        top: -2px;;
                    }
                }
            }
        }
    }
</style>
