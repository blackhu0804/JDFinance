<template lang="html">
    <Panel title="轮播图" :class="$style.panel">
        <section :class="$style.content">
            <Slider :items="items" :cname="$style.slider"/>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
    components: {
        Panel,
        Slider,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22576/78/2157639364/38860/b41902d6/5b7555e8N1f45194c.jpg?width=750&height=400",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t7369/274/3582320735/41472/90f1ae49/5b7555eeN9c6a7d18.jpg?width=750&height=400",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t23137/347/2079098056/27670/1b4a482c/5b7555ebN84129e07.jpg?width=750&height=400",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25591/22/611762283/40092/9771d117/5b7555f1N88557872.jpg?width=750&height=400",
            }],
        }
    },
}
</script>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel {
        @include panel;
        margin: 0 !important;
        >h4 {
            display: none;
        }
        .content {
            margin-top: 120px;
            .slider {
            }
        }
    }
</style>
