<template lang="html">
    <Panel title="领钢镚" :class="$style.panel">
        <section :class="$style.content">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t23131/214/1894630167/24834/62aa0256/5b6c272eN25b66749.gif?width=100&height=100" alt="领钢镚">
        </section>
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
        >h4 {
            display: none;
        }
        .content {
            img {
                width: 100px;
                height: 100px;
                display: block;
                position: fixed;
                right: 40px;
                bottom: 250px;
                z-index: 999;
            }
        }
    }
</style>
