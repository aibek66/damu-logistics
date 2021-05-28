<template>
    <div class="form-section">
        <div class="container">
            <div class="form-content">
                <div class="text-box">
                    <div class="section-title">
                        <h2>Заинтересовала услуга? Заполните форму и мы свяжемся с вами!</h2>
                    </div>

                    <form action="">
                        <div class="input-box">
                            <label for="">Имя*:</label>
                            <input type="text" placeholder="Аскар " />
                        </div>
                        <div class="input-box">
                            <label for="">Номер телефона*:</label>
                            <input type="text" placeholder="+7 (___) ___ __ __ " />
                        </div>
                        <div class="input-box">
                            <label for="">Сопроводительное письмо*:</label>
                            <textarea
                                name=""
                                id=""
                                placeholder="Что именно вас интересует?"
                            ></textarea>
                        </div>
                    </form>
                </div>
                <div class="img-box"></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FormSection'
}
</script>

<style lang="scss" scoped>
.form-section{
    margin-top: 100px;

    .form-content{
        display: grid;

        .text-box{
            padding: 20px;
            background-color: #F7F7F7;
            border-radius: 10px;

            form{
                .input-box{
                    margin-bottom: 30px;
                    &:last-child{
                        margin-bottom: 0;
                    }
                    input,label{
                        display: block;
                    }
                    input, textarea{
                        background: #FFFFFF;
                        border: 1px solid #E3E3E3;
                        border-radius: 10px;
                        font-size: 18px;
                        font-weight: 500;
                        padding: 13px 20px;
                        margin-top: 10px;
                        width: 100%;
                    }
                    textarea{
                        height: 130px;
                    }
                }
            }
        }
    }
}

@media screen and(min-width: 900px){
    .form-section{
        .form-content{
            grid-template-columns: repeat(2,1fr);

            .text-box{
                border-radius: 10px 0px 0px 10px;
                padding: 50px;
                form{
                    .input-box{
                        input,textarea{
                            max-width: 350px;
                        }
                    }
                }
            }

            .img-box{
                border-radius: 0px 10px 10px 0px;
                background-image: url('../assets/hero-section-img.png');
                background-position: center center;
                background-repeat: no-repeat;
                background-size: cover;
            }
        }
    }
}
</style>