<template lang="html">
    <article>
        <Slider :options="options" :items="items" :cname="$style.slider"/>
    </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
    components: { Slider },
    data() {
        return {
            items: [{
                href: "borrowmoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t24235/205/2098418609/15094/1995069a/5b72bdabNfb32c396.png?width=690&height=154",
                title: "最高贷款100万",
            }, {
                href: "borrowmoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25864/7/516309715/16430/d5472d07/5b72bdaeN69689d5e.png?width=690&height=154",
                title: "借钱轻松花",
            }, {
                href: "borrowmoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25285/338/517943235/12882/dddfe757/5b72bdb1N50cc26b6.png?width=690&height=154",
                title: "还款券",
            }, {
                href: "borrowmoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22813/198/2084538556/19837/daa0752e/5b72bdb3Ned42a871.png?width=690&height=154",
                title: "七夕申卡7.7券",
            }, {
                href: "borrowmoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25711/144/495143801/23277/f243587e/5b72bdb6N520501ec.png?width=690&height=154",
                title: "一成首付购车",
            }],
            options: {
                speed: 1500,
                autoplay: true,
                loop: true,
                pagination: {
                    el: ".swiper-pagination",
                },
                notNextTick: false,
            },
        }
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .slider {
        background-color: transparent;
        img {
            width: 100%;
        }
    }
</style>
