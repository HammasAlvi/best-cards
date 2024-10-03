<script>
import HeaderComp from './components/Header.vue';
import MainComp from './components/Main.vue';
import SecMain from './components/SecMain.vue';
import Articles from './components/Articles.vue';
import Links from './components/Links.vue';
import FooterComp from './components/Footer.vue';


export default {
  components: {
    HeaderComp, MainComp , Links , SecMain , Articles , FooterComp
  }
}
</script>

<template>
  <HeaderComp class="header-comp"/>
  <MainComp />
  <Links />
  <SecMain />
  <Articles />
  <a href="#topest">
    <button class="up">-></button>
  </a>
  <FooterComp />
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap");

* {
  margin: 0;
  padding: 0;
}
body {
  background-color: #ffffff;
  box-sizing: border-box;
 
  scroll-behavior: smooth;

}

.up{
  position: sticky;
  left: 1200px;
  bottom: 1200px;
  top: 450px;
  background-color: #141690;
  color: white;
  padding: 12px;
  border: 1px solid white;
  transform: rotate(270deg);
  
}
@media all and (max-width:450px) {
  .up{
  position: sticky;
  left: 400px;
  bottom: 615px;
  top: 450px;
  background-color: #141690;
  color: white;
  padding: 12px;
  border: 1px solid white;
  transform: rotate(270deg); 
} 
}
</style>