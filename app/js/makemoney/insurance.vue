<template lang="html">
    <Panel title="保险保障" :class="$style.panel">
        <section :class="$style.content">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t23200/139/1912146456/46481/f355118d/5b6cf34fN7cfbffb3.jpg?width=750&height=200" alt="">

            <p>热销保险</p>

            <Slider :options="options" :items="items" cname="insurance-slider"/>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
    components: {
        Panel,
        Slider,
    },
    data() {
        return {
            items: [{
                href: "makemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t24889/131/354158065/11634/e9055370/5b6cf2c5N75ddb07d.jpg?width=210&height=260",
            }, {
                href: "makemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t24598/143/363931365/12378/5c52cb7c/5b6cf2e0N00ea6b28.jpg?width=210&height=260",
            }, {
                href: "makemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25219/162/347507731/13524/91dd380a/5b6cf2f8N7a5e9a29.jpg?width=210&height=260",
            }, {
                href: "makemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t23833/191/1845625529/12655/cc8838ca/5b6cf311N15968f23.jpg?width=210&height=260",
            }],
            options: {
                slidesPerView: 2.6,
                spaceBetween: 3,
            }
        }
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .Panel {
        @include panel;
        .content {
            img {
                width: 100%;
            }
            p {
                width: 580px;
                height: 100px;
                margin: 0 auto;
                line-height: 100px;
                text-overflow: ellipsis;
                overflow: hidden;
                white-space: nowrap;
                font-size: 26px;
                color: #666;
            }
        }
    }
</style>
<style lang="scss" scoped>
    .insurance-slider {
        padding-left: 20px;
        padding-bottom: 20px;
    }
</style>
