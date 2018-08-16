<template lang="html">
    <div :class="$style.home">
        <Heador/>
        <Slider/>
        <Novice/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Slider from "./hslider.vue"
import Novice from "./novice.vue"
export default {
    components: {
        Heador,
        Slider,
        Novice,
    },
}
</script>

<style lang="scss" module>
  .home{
    color: red;
    font-size: 40px;
  }
</style>
