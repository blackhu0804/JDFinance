<template lang="html">
    <Panel title="优惠券" :class="$style.panel">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t22930/284/1784613456/150994/5523cb69/5b697d61Nf7756ac1.png?width=750&height=480" alt="">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t16630/362/2707031119/15173/aa5acde3/5b03d5c7Nccffa23f.jpg?width=750&height=480" alt="">
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        @include flex(row);
        margin: 0 !important;
        padding-top: 13px;
        flex-wrap: nowrap;
        img {
            width: 320px;
            height: 204px;
        }
    }
</style>
