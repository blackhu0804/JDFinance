<template lang="html">
    <Panel title="有车有钱" :class="$style.panel">
        <h3>有车有钱</h3>
        <section :class="$style.content">
            <div :class="$style.imgBox">
                <img src="https://img12.360buyimg.com/jrpmobile/jfs/t22774/46/1735806175/76049/3a394283/5b690b9aN054ad12e.png?width=375&height=233" alt="">
                <img src="https://img12.360buyimg.com/jrpmobile/jfs/t14215/140/1757206721/24186/81b4e53c/5a56c877Nee6cfc4d.jpg?width=375&height=233" alt="">
            </div>
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
        padding-top: 42.5px;
        margin-bottom: 0 !important;
        > h3 {
            color: #000;
            font-weight: 500;
            margin: 0 26px 26px;
            padding-left: 18px;
            font-size: 30px;
            position: relative;
            &:before {
                content: '';
                position: absolute;
                left: 4px;
                width: 5px;
                height: 31px;
                background: url("https://m.jr.jd.com/vip/borrowMoney/css/i/title.png") 0 0 no-repeat;
            }
        }
        > h4 {
            display: none;
        }
        .content {
            .imgBox {
                width: 100%;
                padding-bottom: 42.5px;
                @include flex(row);
                img {
                    width: 50%;
                }
            }
        }
    }
</style>
