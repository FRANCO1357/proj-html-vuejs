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
    BaseFooter,
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
@import "./assets/sass/style.scss";
</style>
