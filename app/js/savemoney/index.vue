<template lang="html">
    <div :class="$style.home">
        <Heador/>
        <Slide/>
        <Slider/>
        <Coupon/>
        <Pay/>
        <Life/>
        <Ad/>
        <Crowd/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Navbar from "../public/navbar.vue"
import Slide from "./sslider.vue"
import Slider from "./sslideb.vue"
import Coupon from "./coupon.vue"
import Pay from "./pay.vue"
import Life from "./life.vue"
import Ad from "./ad.vue"
import Crowd from "./crowd"
export default {
    components: {
        Heador,
        Navbar,
        Slide,
        Slider,
        Coupon,
        Pay,
        Life,
        Ad,
        Crowd,
    },
}
</script>

<style lang="scss" module>
    .home{
        font-size: 40px;
    }
</style>
