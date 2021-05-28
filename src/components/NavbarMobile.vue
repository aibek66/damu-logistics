<template>
    <div class="container">
    <nav>
        <img class="logo" src="../assets/logo.png" alt="" />
        <ul :class="{'show': clicked}" class="navbar-menu">
            <li @click="handleClick">
                <router-link to="/">
                    О нас
                    <img src="../assets/up-arrow.svg" alt="up-arrow" />
                </router-link>
            </li>
            <li @click="handleClick">
                <router-link to="/">
                    Резиденты
                </router-link>
            </li>
            <li @click="handleClick" class="active">
                <router-link to="/">Услуги и сервис</router-link>
                
            </li>
            <li @click="handleClick">
                <router-link to="/">
                    Карьера
                </router-link>
            </li>
            <li @click="handleClick">
                <router-link to="/">
                    Закупки
                </router-link>
            </li>
            <li @click="handleClick">
                <router-link to="/">
                    Контакты
                </router-link>
            </li>
            <li @click="handleClick">
                <router-link to="/">
                    RU
                    <img src="../assets/up-arrow.svg" alt="up-arrow" />
                </router-link>
            </li>
        </ul>
        <img @click="handleClick" v-if="!clicked" class="menu-icon" src="../assets/menu-icon.svg" alt="" />
        <img @click="handleClick" v-if="clicked" class="menu-icon" src="../assets/x-icon.svg" alt="" />
    </nav>
    </div>
</template>

<script>
export default {
    name: 'NavbarMobile',
    data(){
        return{
            clicked: false,
        }
    },
    methods:{
        handleClick(){
            this.clicked = !this.clicked;
            this.clicked ? (document.body.style.overflow='hidden') : (document.body.style.overflow='');
        }
    },
}
</script>

<style lang="scss" scoped>
nav{
    display: flex;
    justify-content: space-between;
    padding: 30px 0;
    .logo,.menu-icon{
        z-index: 5;
    }
    ul{
        overflow: hidden;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        transition: .3s ease-in-out;
        position: absolute;
        top: 120px;
        left: -100%;
        height: calc(100vh - 120px);
        background-color: khaki;
        z-index: 3;
        &.show{
            left: 0;
        }
        li,a{
            font-size: 20px;
            cursor: pointer;
            display: flex;
            align-items: center;
            color: #231F20;
            margin: 15px 0;
            img{
                margin-left: 10px;
            }
            &.active{
                position: relative;
                &::after{
                    content: '';
                    position: absolute;
                    bottom: 0;
                    width: 100%;
                    height: 5px;
                    background-color: #8CC240;
                    border-radius: 2.5px 2.5px 0px 0px;
                }
            }
        }
    }
}
</style>