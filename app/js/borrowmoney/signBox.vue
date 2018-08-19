<template lang="html">
    <router-link :to="{name: 'borrowmoney'}">
        <div :class="$style.signBox"/>
    </router-link>
</template>

<script>

</script>

<style lang="scss" module>
    .signBox {
        width: 104px;
        height: 136px;
        background: url("//m.jr.jd.com/vip/borrowMoney/widget/jdGold/i/signIcon.png") 0 0 no-repeat;
        background-size: 100% 100%;
        position: fixed;
        right: -25px;
        top: 60%;
        z-index: 10;
    }
</style>
