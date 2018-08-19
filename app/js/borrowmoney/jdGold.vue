<template lang="html">
    <Panel title="京东金条" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.gold">
                <img src="//m.jr.jd.com/vip/borrowMoney/widget/jdGold/i/goldCard.png" alt="京东金条">
                <p>最高可借</p>
                <p><span>￥</span>300,000</p>
                <p>立即登陆</p>
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
        background-color: transparent;
        .content {
            width: 100%;
            padding: 47px 26px 0;
            box-sizing: border-box;
            .gold {
                position: relative;
                img {
                    width: 100%;
                }
                p {
                    position: absolute;
                    color: #fff;
                    &:first-of-type {
                        top: 18%;
                        left: 10%;
                        font-size: .7rem;
                    }
                    &:nth-of-type(2) {
                        top: 30%;
                        left: 9%;
                        font-size: 70px;
                        text-shadow: 0 0.3125rem 0.3125rem rgba(63,39,0,.2);
                        span {
                            font-size: 50px;
                        }
                    }
                    &:last-of-type {
                        top: 56%;
                        left: 10%;
                        font-size: 26px;
                        text-align: center;
                        line-height: 57px;
                        font-weight: 500;
                        background: url("https://m.jr.jd.com/vip/borrowMoney/widget/jdGold/i/btnBj.png") 0 0 no-repeat;
                        width: 180px;
                        height: 57px;
                        background-size: 100% 100%;
                    }
                }
            }
        }
    }
</style>
