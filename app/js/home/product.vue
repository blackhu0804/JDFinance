<template lang="html">
    <Panel title="新品推荐" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.arrow">
                更多尖货 >
            </div>
            <Slider :options="options" :items="items" cname="product-slider"/>
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
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t21691/233/2361780032/59932/8cb4ce42/5b5066e3Nb460c234.jpg?width=335&height=421",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t24547/3/1113130809/37409/3e7d5038/5b5066f2N360c723a.jpg?width=335&height=421",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22696/182/1419336545/44627/3e46409d/5b5fcdb3N4c31020e.jpg?width=335&height=421",
            }],
            options: {
                slidesPerView: 2.3,
                spaceBetween: 30,
            },
        }
    },
}
</script>

<style lang="scss">
    .product-slider {
        .swiper-container {
            -webkit-box-sizing: border-box;
            -moz-box-sizing: border-box;
            box-sizing: border-box;
            padding: 0 24px;
            .swiper-slide {
                a {
                    display: inline-block;
                    width: 100%;
                    img {
                        width: 100%;
                        display: block;
                        height: 314px;
                        border: 1px solid #fafafa;
                    }
                }
            }
        }
    }
</style>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        .content {
            padding-bottom: 40px;
            position: relative;
            &>div {
                position: absolute;
                font-size: 28px;
                color: #999;
                right: 20px;
                top: -70px;
            }
        }
    }
</style>
