<template>
  <div>
    <NavbarMobile v-if="mobileView" />
    <Header v-if="!mobileView" />
    <router-view/>
    <Footer />
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import NavbarMobile from './components/NavbarMobile.vue'

export default {
  name: 'App',
  components:{
    Header,
    Footer,
    NavbarMobile
  },
  data(){
    return{
      mobileView: false,
    }
  },
  methods:{
    handleView (){
      this.mobileView = window.innerWidth <= 992;
    }
  },
  created(){
    this.handleView();
    window.addEventListener('resize', this.handleView);
  }
}
</script>

<style lang="scss">
*{
	margin: 0;
	padding: 0;

	box-sizing: border-box;
}

html,
body {
	font-family: 'Montserrat', sans-serif;
}

input, button, textarea{
	font-family: inherit;
	outline: none;
}

a{
  text-decoration: none;
}

ul{
	list-style: none;
}

h1{
	font-size: 28px;
	font-weight: 700;
	line-height: 39px;
}

h2{
	font-size: 24px;
	font-weight: 700;
	line-height: 33px;
}

h3{
	font-size: 20px;
	font-weight: 700;
	line-height: 28px;
}

p{
	font-size: 18px;
	font-weight: 500;
	line-height: 25px;
}

button{
	font-size: 16px;
	font-weight: 600;
	padding: 11px 24px;
	border: none;
	border-radius: 10px;
}

.header-container{
	max-width: 1300px;
	width: 90%;
	margin: 0 auto;
	padding: 30px 0;
}

.container{
  max-width: 1110px;
  width: 90%;
  margin: 0 auto;
}

.section-title{
	h1{
		margin-bottom: 15px;
	}
	margin-bottom: 30px;
}

.btn-primary{
	color: #fff;
	background-color: rgba(140, 194, 64, 1);
}
</style>
