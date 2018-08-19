<template lang="html">
    <div :class="$style.home">
        <Heador/>
        <Navbar/>
        <JdGold/>
        <Slider/>
        <HavaCar/>
        <NavSlide/>
        <Note/>
        <Activity/>
        <SignBox/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Navbar from "../public/navbar.vue"
import JdGold from "./jdGold.vue"
import Slider from "./bslider.vue"
import HavaCar from "./haveCar.vue"
import NavSlide from "./navSlider.vue"
import Note from "./note.vue"
import Activity from "./activity.vue"
import SignBox from "./signBox.vue"
export default {
    components: {
        Heador,
        Navbar,
        JdGold,
        Slider,
        HavaCar,
        NavSlide,
        Note,
        Activity,
        SignBox,
    },
}
</script>

<style lang="scss" module>
    .home {
        font-size: 40px;
        background: url("//m.jr.jd.com/vip/borrowMoney/css/i/bj.png");
        background-size: 100% auto;
    }
</style>
