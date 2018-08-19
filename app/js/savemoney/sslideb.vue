<template lang="html">
    <Swiper :items="items" :class="$style.content" />
</template>

<script>
import Swiper from "../core/slider.vue"
export default {
    components: {
        Swiper,
    },
    data() {
        return {
            items: [{
                href: "savemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25810/47/597579774/62665/9b06690d/5b755812Nc36feb8c.jpg?width=750&height=360",
            }, {
                href: "savemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t24280/56/1656945012/39815/e5df9db8/5b641744Nd33d2e71.jpg?width=750&height=360",
            }, {
                href: "savemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22693/60/1469215837/31938/10fd7920/5b618d2aN7b9a6ef9.jpg?width=750&height=360",
            }, {
                href: "savemoney",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t20794/355/2486516652/67537/4643f0b8/5b57da12N354a4309.jpg?width=750&height=360",
            }],
        }
    },
}
</script>

<style lang="scss" module>
    .content {
        img {
            width: 100%;
        }
    }
</style>
