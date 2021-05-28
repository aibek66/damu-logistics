<template>
    <div class="services">
        <div class="container">
            <div class="section-title">
                <h2>Другие услуги</h2>
            </div>

            <swiper
                class="swiper-container"
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
                        slidesPerView: 4
                    }
                }"
            >
                <swiper-slide>
                    <h3>Строительство</h3>
                </swiper-slide>
                <swiper-slide>
                    <h3>Фармацевтика и здравоохранение</h3>
                </swiper-slide>
                <swiper-slide>
                    <h3>Транспортная логистика</h3>
                </swiper-slide>
                <swiper-slide>
                    <h3>Оборонная промышленность</h3>
                </swiper-slide>
                <swiper-slide>
                    <h3>Автопромышленность</h3>
                </swiper-slide>
                <swiper-slide>
                    <h3>Бытовая техника и электроника</h3>
                </swiper-slide>
                <img class="swiper-button-prev"  src="../assets/slider-arrow.svg" alt="" />
                <img class="swiper-button-next" src="../assets/slider-arrow.svg" alt="" />
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
        name: 'Services',
        components: {
            Swiper,
            SwiperSlide,
        },
    }    
</script>

<style lang="scss" scoped>
.services{
    margin-top: 100px;
    position: relative;

    .btn-box{
        display: flex;
        justify-content: center;
        button{
            margin-top: 50px;
        }
    }


    .swiper-wrapper{
        position: unset;
    }

    .swiper-slide{
        height: 200px;
        border-radius: 10px;

        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
        text-align: center;
        h3{
            color: #fff;
            display: inline-block;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        &:nth-child(1){
            background-image: url('../assets/services-img1.png');
        }
        &:nth-child(2){
            background-image: url('../assets/services-img6.png');
        }
        &:nth-child(3){
            background-image: url('../assets/services-img5.png');
        }
        &:nth-child(4){
            background-image: url('../assets/services-img3.png');
        }
        &:nth-child(5){
            background-image: url('../assets/services-img4.png');
        }
        &:nth-child(6){
            background-image: url('../assets/services-img2.png');
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
    }
    .swiper-button-next{
        transform: rotate(180deg);
        right: 1%;
    }
    .swiper-button-prev{
        left: 1%;
    }
}

@media screen and (min-width: 768px){
    .services{
        .swiper-container{
            position: unset;
        }
    }
}

@media screen and (min-width: 1400px){
    .services{
        .swiper-button-next{
            right: 7%;
        }
        .swiper-button-prev{
            left: 7%;
        }
    }
}
</style>