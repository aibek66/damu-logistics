<template>
    <footer>
        <div class="container">
            <div class="content">
                <div class="item">
                    <img src="../assets/logo.png" alt="" />
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
                    <div class="social-icons">
                        <img src="../assets/Instagram.png" alt="" />
                        <img src="../assets/LinkedIn.png" alt="" />
                        <img src="../assets/Facebook.png" alt="" />
                        <img src="../assets/YouTube.png" alt="" />
                        <img src="../assets/Telegram.png" alt="" />
                    </div>
                </div>

                <div class="item">
                    <h3>КАРТА САЙТА</h3>
                    <ul>
                        <li>О нас</li>
                        <li>Инвесторам</li>
                        <li>Резиденты</li>
                        <li>Услуги и сервис</li>
                        <li>Карьера</li>
                        <li>Закупки</li>
                        <li>Новости</li>
                        <li>Контакты</li>
                    </ul>
                </div>

                <div class="item">
                    <h3>КОНТАКТЫ</h3>
                    <ul>
                        <li>+7 (727) 312-12-11</li>
                        <li>info@dlg.kz</li>
                        <li>
                            Алматинская область, Илийский район, п. Байсерке, ул.
                            Султана-Бейбарса 1
                        </li>
                    </ul>
                </div>
            </div>
        </div>
	</footer>
</template>

<script>
    export default{
        name: 'Footer'
    }
</script>

<style scoped lang="scss">
footer{
    margin-top: 50px;
    background-color: #F8F8F8;
    padding: 100px 0;

    .content{
        display: flex;
        flex-direction: column;
        .item{
            margin-top: 50px;
            flex: 1;
            color: rgba(35, 31, 32, 1);
            p{
                font-size: 16px;
                font-weight: 500;
                line-height: 22px;
            }

            h3{
                font-size: 16px;
                font-weight: 600;
            }

            &:first-child{
                margin-top: 0;
                p{
                    margin: 20px 0 40px;
                }

                .social-icons{
                    img{
                        margin-right: 25px;
                        &:last-child{
                            margin-right: 0;
                        }
                    }
                }
            }

            ul{
                margin-top: 10px;
                li{
                    margin-top: 20px;
                    cursor: pointer;
                }
            }
        }
    }
}

@media screen and(min-width:992px){
    footer{
        .content{
            flex-direction: row;
            flex-wrap: wrap;
            .item{
                margin-top: 0;
            }
        }
    }
}
</style>