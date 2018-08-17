<template lang="html">
    <Panel title="白条服务" :class="$style.panel">
        <h3>白条服务</h3>
        <section :class="$style.content">
            <img src="https://m.jr.jd.com/vip/borrowMoney/widget/bannerAndCar/i/whiteCard.png" alt="">
            <div :class="$style.credit">
                <img src="https://m.jr.jd.com/vip/borrowMoney/widget/bannerAndCar/i/whiteCircle.png" alt="">
                <p>登陆查看</p>
                <em>小白信用</em>
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
        margin: 0;
        &:before {
            content: '';
            width: 100%;
            height: 17px;
            background-color: #f3f5f7;
            display: block;
        }
        > h3 {
            padding-top: 42.5px;
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
            @include flex(row);
            padding: 0 13px;
            >img {
                width: 393px;
                height: 262px;
            }
            .credit {
                position: relative;
                img {
                    width: 217px;
                    height: 262px;
                }
                p {
                    position: absolute;
                    font-size: 24px;
                    color: #ae8339;
                    top: 65.5%;
                    left: 27%;
                }
                em {
                    position: absolute;
                    font-size: 24px;
                    top: 36%;
                    color: #ffeac9;
                    left: 27%;
                }
            }
        }
    }
</style>
