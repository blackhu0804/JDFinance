<template lang="html">
    <Panel title="Ad" :class="$style.panel">
        <section :class="$style.content">
            <h2>钱的事 京东金融很行</h2>
            <h3>源于京东 更源于信任</h3>
            <img src="//img30.360buyimg.com/jr_image/jfs/t19984/55/863040802/115952/7b1125fa/5b0d4b6dN621644ea.png" alt="">
        </section>
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
        padding-top: 55px;
        >h4 {
            display: none;
        }
        .content {
            h2 {
                font-size: 30px;
                text-align: center;
                color: rgb(40, 48, 57);
                margin-bottom: 7px;
                height: 45px;
                line-height: 45px;
            }
            h3 {
                color: rgb(131, 145, 167);
                font-size: 22px;
                text-align: center;
                height: 30px;
                line-height: 30px;
            }
            img {
                width: 100%;
            }
        }
    }
</style>
