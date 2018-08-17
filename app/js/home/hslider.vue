<template lang="html">
    <article>
        <Slider :items="items" :cname="$style.slider"/>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{ name: item.href }">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{ item.title }}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
    components: { Slider },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25195/34/538079874/44233/59252c2e/5b72bdc0N8cbe97c9.jpg?width=750&height=320",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t24187/24/2107306777/42617/896ed155/5b741129Nb4983492.jpg?width=750&height=320",
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t23983/288/2084923913/46101/c757ce61/5b72bde6Naadd64f4.jpg?width=750&height=320",
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t25570/320/540292612/45517/320d04c3/5b72bdebN6b0c25b9.jpg?width=750&height=320",
            }],
            enters: [{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                title: "优惠券",
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                title: "领福利",
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                title: "抢钢镚",
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                title: "白条提额",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
    .slider {
        margin-top: 120px;
        img {
            width: 100%;
        }
    }
    .list {
        @include list(row);
        background: #ffffff;
        padding-top: 40px;
        padding-bottom: 20px;
        justify-content: space-around;
        a {
            text-decoration: none;
        }
        .item {
            text-align: center;
            img {
                display: inline-block;
                height: 90px;
                width: 90px;
            }
            h4 {
                font-size: 26px;
                margin-top: 12px;
                color: #666;
            }
        }
        .item:nth-of-type(3) {
            h4 {
                color: #ff0000;
            }
        }
    }
</style>
