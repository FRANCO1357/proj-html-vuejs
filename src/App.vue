<template>
  <div>
    <BaseHeader :links="menuLinks"/>
    <TheJumbotron :icons="jumbotronIcons"/>
    <BaseMain :courses="coursesList" :benefits="benefitsList" :testimonials="testimonialsList" :brandData="brandData" :blogsArticles="blogsArticles"/>
    <BaseFooter :footerMenuLinks="footerMenuLinks"/>
  </div>
</template>

<script>
import { menuLinks, jumbotronIcons, coursesList, benefitsList, testimonialsList, brandData, blogsArticles, footerMenuLinks } from './assets/data/index.js';
import BaseHeader from './components/BaseHeader.vue';
import BaseMain from './components/BaseMain.vue';
import TheJumbotron from './components/TheJumbotron.vue';
import BaseFooter from './components/BaseFooter.vue';

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain,
    TheJumbotron,
    BaseFooter
},
  data(){
    return{
      menuLinks,
      jumbotronIcons,
      coursesList,
      benefitsList,
      testimonialsList,
      brandData,
      blogsArticles,
      footerMenuLinks,
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
