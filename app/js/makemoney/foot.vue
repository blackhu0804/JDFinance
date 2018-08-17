<template lang="html">
    <Panel title="京东金融出品" :class="$style.panel">
        a
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
        > h4 {
            color: #b1b4bb;
            height: 100px;
            line-height: 100px;
            background-color: #f5f5f5;
            padding-bottom: 140px;
            font-weight: normal;
            font-size: 24px;
        }
    }
</style>
