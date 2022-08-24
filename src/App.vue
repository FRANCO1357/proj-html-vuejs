<template>
  <div>
    <BaseHeader :links="menuLinks"/>
    <TheJumbotron :icons="jumbotronIcons"/>
    <BaseMain :courses="coursesList" :benefits="benefitsList"/>
  </div>
</template>

<script>
import { menuLinks, jumbotronIcons, coursesList, benefitsList } from './assets/data/index.js';
import BaseHeader from './components/BaseHeader.vue';
import BaseMain from './components/BaseMain.vue';
import TheJumbotron from './components/TheJumbotron.vue';

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain,
    TheJumbotron
},
  data(){
    return{
      menuLinks,
      jumbotronIcons,
      coursesList,
      benefitsList,
    }
  }
}
</script>

<style lang="scss" >
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;

    body{
      font-family: 'Poppins', sans-serif;    

          ul li{
      list-style-type: none;

      a{
        text-decoration: none;
        color: black;
      }
    }

    img{
      max-width: 100%;
    }

    .container{
      width: 1200px;
      margin: 0 auto;
      padding: 20px;
    }
    }


  }
</style>
