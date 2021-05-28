<template>
    <div class="hero-section">
        <div class="container">
            <div class="section-title">
                <h1>Бытовая техника и электроника</h1>
                <p>
                    Мы являемся несомненными лидерами в предоставлении комплексных решений для
                    компаний в сфере производства и поставок бытовой техники и электроники.
                </p>
            </div>
            <div class="img-box"></div>
            <div class="text-boxes">
                <div class="item">
                    <div class="box">
                        <p>
                            Начиная от контроля поставок из стран Юго-Восточной Азии, Европы и
                            ЕАЭС, наши логистические терминалы могут являться
                            распределительными, кросс-докинговыми центрами.
                        </p>
                        <p class="box-number">01</p>
                    </div>
                    <div class="box">
                        <p>
                            Мы предлагаем полный сервис с предпродажной подготовкой и сборкой
                            товара (проверкой и переборкой брака, отслеживанием партий и
                            серийных номеров, упаковкой, вложением инструкций и описаний на
                            необходимых языках). Это который создадут основу для эффективного
                            построения всей логистической цепочки.
                        </p>
                        <p class="box-number">02</p>
                    </div>
                </div>
                <div class="item">
                    <div class="box">
                        <p>
                            Мы обеспечим прием всех видов транспорта с оформлением
                            разрешительных документов и таможенной очистки в одной локации с
                            последующей отправкой товара "до двери" по всему миру, что позволит
                            эффективно распределить ресурсы и своевременно поставить товар Вашим
                            партнерам, сократив сроки и сэкономив дополнительные средства для
                            развития бизнеса.
                        </p>
                        <p class="box-number">03</p>
                    </div>

                    <div class="box">
                        <p>
                            Индустриальные парки DAMU Logistics могут построить заводы по
                            производству и сборке техники и электроники, что позволит не только
                            завоевать рынок, но и оптимизировать многие процессы.
                        </p>
                        <p class="box-number">04</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeroSection'
}
</script>

<style scoped lang="scss">
.hero-section{
    margin-top: 60px;
    .img-box{
        width: 100%;
        height: 400px;
        background-image: url('../assets/hero-section-img.png');
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        border-radius: 10px;
    }

    .text-boxes{
        margin-top: 50px;
        display: grid;
        grid-gap: 30px;
        .item{
            display: grid;
            grid-row-gap: 30px;
        }
        .box{
            background-color: #fff;
            box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            padding: 30px;
            position: relative;

            &-number{
                position: absolute;
                right: 10px;
                bottom: 20px;

                font-size: 72px;
                font-weight: 800;
                color: #EAEAEA;
                z-index: 0;
            }
        }
    }
}

@media screen and(min-width: 768px){
    .hero-section{
        .text-boxes{
            grid-template-columns: repeat(2,1fr);
            align-items: flex-start;
        }
    }
}
</style>