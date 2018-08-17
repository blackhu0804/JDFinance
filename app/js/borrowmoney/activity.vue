<template lang="html">
    <Panel title="精品活动" :class="$style.panel">
        <h3>精品活动</h3>
        <section :class="$style.content">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t23692/129/277307053/51270/85a1db60/5b2af9c0N7a15f0c2.png?width=376&height=264" alt="">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t22264/337/1504407440/65624/b7d95603/5b2afbeaN7987d0b2.png?width=376&height=264" alt="">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t16675/365/91110617/54621/c0042c09/5a5c87faNd161d42e.png?width=730&height=264" alt="">
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
        > h4 {
            display: none;
        }
        > h3 {
            height: 112px;
            padding: 0 32px;
            line-height: 112px;
            font-size: 32px;
            font-weight: 700;
            color: #333333;
        }
        .content {
            @include flex(row);
            img:first-child, img:nth-child(2) {
                width: 50%;
                box-sizing: border-box;
            }
            img:last-child {
                width: 100%;
            }
            padding-bottom: 100px;
        }
    }
</style>
