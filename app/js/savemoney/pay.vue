<template lang="html">
    <Panel title="支付优惠" :class="$style.panel">
        <h3>支付优惠</h3>
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t20125/139/377044579/41214/51a08cb6/5b0b947bN916e62ee.jpg?width=1500&height=442" alt="">
        <div :class="$style.content">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t21220/114/370135108/16076/707215c1/5b0b957bNcb388c1b.png?width=335&height=420" alt="">
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t19198/45/2659881364/38954/a2c7ccc1/5b0402a7Nc06d77e4.png?width=335&height=210" alt="">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t23230/230/1801176631/6182/4c369cf4/5b6aa7f2N7d9543dd.png?width=335&height=200" alt="">
            </div>
        </div>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        box-sizing: border-box;
        >h4 {
            display: none;
        }
        > img {
            width: 100%;
        }
        .content {
            @include flex(row);
            flex-wrap: nowrap;
            padding: 0 30px;
            > img {
                width: 280px;
                height: 363px;
                border-right: 10px solid #f5f5f5;
            }
            .item {
                img {
                    width: 280px;
                    height: 182px;
                    border-left: 10px solid #f5f5f5;
                    &:first-child {
                        border-bottom: 20px solid #f5f5f5;
                    }
                }
            }
        }
    }
</style>
