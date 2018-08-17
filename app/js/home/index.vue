<template lang="html">
    <div :class="$style.home">
        <Heador/>
        <Slider/>
        <Novice/>
        <Borrow/>
        <Money/>
        <Product/>
        <Insurance/>
        <Life/>
        <Foot/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Foot from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./hslider.vue"
import Novice from "./novice.vue"
import Borrow from "./borrow.vue"
import Money from "./money.vue"
import Product from "./product.vue"
import Insurance from "./insurance.vue"
import Life from "./life.vue"
export default {
    components: {
        Heador,
        Slider,
        Novice,
        Borrow,
        Money,
        Product,
        Insurance,
        Life,
        Foot,
        Navbar,
    },
}
</script>

<style lang="scss" module>
  .home{
    color: red;
    font-size: 40px;
  }
</style>
