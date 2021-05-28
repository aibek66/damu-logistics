<template>
    <header class="header">
			<div class="header-container">
				<nav>
					<ul class="navbar-menu">
						<li>
                            <router-link to="/about">
                                О нас
                                <img src="../assets/up-arrow.svg" alt="up-arrow" />
                            </router-link>
						</li>
						<li>
                            <router-link to="/">
                                Резиденты
                            </router-link>
                        </li>
						<li class="active">
                            <router-link to="/">Услуги и сервис</router-link>
                            
                        </li>
						<li class="menu-logo">
                            <router-link to="/">
                                <img src="../assets/logo.png" alt="logo" />
                            </router-link>
                        </li>
						<li>
                            <router-link to="/">
                                Карьера
                            </router-link>
                        </li>
						<li>
                            <router-link to="/">
                                Закупки
                            </router-link>
                        </li>
						<li>
                            <router-link to="/">
                                Контакты
                            </router-link>
                        </li>
						<li>
                            <router-link to="/">
							    RU
							    <img src="../assets/up-arrow.svg" alt="up-arrow" />
                            </router-link>
						</li>
					</ul>
				</nav>
			</div>
		</header>
</template>

<script>
    export default {
        name: 'Header',
    }
</script>

<style scoped lang="scss">
.header{
    max-width: 1410px;
    margin: 0 auto;
    background-color: #fff;
    box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    nav{

        display: flex;
        justify-content: space-between;
        ul{
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            li,a{
                font-size: 16px;
                cursor: pointer;
                display: flex;
                align-items: center;
                color: #231F20;
                img{
                    margin-left: 10px;
                }
                &.active{
                    position: relative;
                    &::after{
                        content: '';
                        position: absolute;
                        top: 25px;
                        width: 100%;
                        height: 5px;
                        background-color: #8CC240;
                        border-radius: 2.5px 2.5px 0px 0px;
                    }
                }
            }
        }
    }
}
</style>

