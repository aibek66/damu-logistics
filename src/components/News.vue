<template>
    <div class="news">
        <div class="container">
            <div class="section-title">
                <h2>Последние новости</h2>
                <div class="line"></div>
            </div>

            <swiper
                class="swiper-container news-slider"
                :slides-per-view="1"
                :space-between="30"
                :navigation="{
                    nextEl: '.swiper-button-next',
                    prevEl: '.swiper-button-prev'
                }"
                :breakpoints="{
                    768: {
                        slidesPerView: 2,
                    },
                    992: {
                        slidesPerView: 3
                    }
                }"
            >
                <swiper-slide class="swiper-slide">
                    <div class="img-box"></div>
                    <p>12.02.2021</p>
                    <h3>Индустриальный парк</h3>
                </swiper-slide>
                <swiper-slide class="swiper-slide">
                    <div class="img-box"></div>
                    <p>12.02.2021</p>
                    <h3>
                        Сотрудники DAMU Logistics вручили детям 20 смартфонов для
                        дистанционного обучения.
                    </h3>
                </swiper-slide>
                <swiper-slide class="swiper-slide">
                    <div class="img-box"></div>
                    <p>12.02.2021</p>
                    <h3>Автоматизация и международные стандарты McDonald’s</h3>
                </swiper-slide>
                <swiper-slide class="swiper-slide">
                    <div class="img-box"></div>
                    <p>12.02.2021</p>
                    <h3>Индустриальный парк</h3>
                </swiper-slide>
                <swiper-slide class="swiper-slide">
                    <div class="img-box"></div>
                    <p>12.02.2021</p>
                    <h3>Автоматизация и международные стандарты McDonald’s</h3>
                </swiper-slide>
                <img class="swiper-button-prev" src="../assets/slider-arrow.svg" alt="" />
                <img class="swiper-button-next" src="../assets/arrow-right.svg" alt="" />
            </swiper>

            <div class="btn-box">
                <button class="btn-primary">Показать все</button>
            </div>
        </div>
    </div>
</template>

<script>
    import SwiperCore, { Navigation, } from 'swiper';

    // Import Swiper Vue.js components
    import { Swiper, SwiperSlide } from 'swiper/vue';

    // Import Swiper styles
    import 'swiper/swiper.scss';
    import 'swiper/components/navigation/navigation.scss';

    // install Swiper modules
    SwiperCore.use([Navigation]);
export default {
    name: 'News',
    components: {
        Swiper,
        SwiperSlide,
    },
}
</script>

<style lang="scss" scoped>
.news{
    margin-top: 100px;
    position: relative;

    .section-title{
        display: flex;
        align-items: center;
        .line{
            flex: 1;
            height: 1px;
            background-color: rgba(123, 121, 121, 1);
            margin-left: 20px;
        }
    }

    .swiper-wrapper{
        position: unset;
    }

    .swiper-slide{
        .img-box{
            width: 100%;
            height: 248px;
            background-image: url('../assets/services-img1.png');
            border-radius: 10px;
            background-repeat: no-repeat;
            background-size: cover;
        }

        &:nth-child(2){
            .img-box{
                background-image: url('../assets/services-img4.png');
            }
        }

        &:nth-child(3){
            .img-box{
                background-image: url('../assets/services-img3.png');
            }
        }

        p{
            margin: 15px 0 10px;
            font-size: 16px;
            font-weight: 500;
            color: rgba(123, 121, 121, 1);
        }

        h3{
            font-size: 18px;
            font-weight: 700;
            line-height: 25px;
        }
    }

    .swiper-button-prev,.swiper-button-next{
        width: 24px;
        height: 24px;
        background-color: rgba(140, 194, 64, 1);
        border-radius: 50%;
        padding: 4px;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        z-index: 10;
    }
    .swiper-button-next{
        right: 1%;
    }
    .swiper-button-prev{
        left: 1%;
    }

    .btn-box{
        display: flex;
        justify-content: center;
        button{
            margin-top: 50px;
        }
    }
}

@media screen and (min-width: 768px){
    .news{
        &-slider{
            position: unset;
        }
    }
}

@media screen and (min-width: 1400px){
    .news{
        .swiper-button-next{
            right: 7%;
        }
        .swiper-button-prev{
            left: 7%;
        }
    }
}
</style>