<template lang="html">
    <Panel title="下载APP" :class="$style.panel">
        <section :class="$style.content">
            <div>
                <img src="//m.jr.jd.com/spe/downloadApp/css/i/logo.png" alt="">
                <p>会赚钱 懂生活的人都在这里</p>
                <section :class="$style.btn">
                    立即下载
                </section>
                <p>打开京东金融 ></p>
            </div>
            <section :class="$style.by"><img src="//m.jr.jd.com/spe/downloadApp/css/i/by.png" alt=""></section>
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
    html, body {
        background-color: #fff;
    }
    .panel {
        @include panel;
        margin: 0 !important;
        background-image: -webkit-linear-gradient(269deg,#F02 0,#FF722E 100%);
        background-image: linear-gradient(-179deg,#F02 0,#FF722E 100%);
        position: relative;
        > h4 {
            display: none;
        }
        .content {
            background: url("//m.jr.jd.com/spe/downloadApp/css/i/bg.png") no-repeat 50% 0/100% auto;
            padding: 114px 0;
            >div {
                @include flex;
                justify-content: center;
                align-items: center;
                img {
                    width: 180px;
                    height: 202px;
                }
                p:first-of-type {
                    font-size: 25px;
                    margin-top: 17px;
                    color: rgba(255,255,255,.6);
                }
                .btn {
                    width: 430px;
                    height: 85px;
                    margin: 130px auto 0;
                    background-color: #fff;
                    box-shadow: 0 0.3125rem 0.625rem 0 #FF622B;
                    border-radius: 5px;
                    text-align: center;
                    line-height: 85px;
                    color: #FF552B;
                    font-size: 29px;
                }
                p:nth-of-type(2) {
                    color: #fff;
                    font-size: 24px;
                    text-align: center;
                    margin-top: 46px;
                }
            }
            .by {
                position: absolute;
                left: 0;
                right: 0;
                bottom: -10px;
                img {
                    width: 100%;
                    height: 100%;
                }
            }
        }
    }
</style>
