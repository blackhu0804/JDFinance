<template lang="html">
    <div :class="$style.home">
        <Heador/>
        <Slider/>
        <Ada/>
        <Money/>
        <Insurance/>
        <Recommend/>
        <Foot/>
        <Navbar/>
        <Specie/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./mslider.vue"
import Ada from "./ada.vue"
import Specie from "./specie.vue"
import Money from "./money.vue"
import Insurance from "./insurance.vue"
import Recommend from "./recommend.vue"
import Foot from "./foot.vue"
export default {
    components: {
        Heador,
        Slider,
        Foot,
        Navbar,
        Ada,
        Specie,
        Money,
        Insurance,
        Recommend,
    },
}
</script>

<style lang="scss" module>
    .home{
        font-size: 40px;
    }
</style>
