<template>
  <div>
    <BaseHeader :links="menuLinks"/>
    <TheJumbotron :icons="jumbotronIcons"/>
    <BaseMain :courses="coursesList"/>
  </div>
</template>

<script>
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
      menuLinks: [
        { text: "Menù", href: "#" },
        { text: "Pages", href: "#" },
        { text: "Courses", href: "#" },
        { text: "Features", href: "#" },
        { text: "Blog", href: "#" },
        { text: "Shop", href: "#" },
      ],
      jumbotronIcons: [
        { src: require("./assets/images/client-logo-01.png"), alt: "client-01" },
        { src: require("./assets/images/client-logo-02.png"), alt: "client-02" },
        { src: require("./assets/images/client-logo-03.png"), alt: "client-03" },
        { src: require("./assets/images/client-logo-04.png"), alt: "client-04" },
        { src: require("./assets/images/client-logo-05.png"), alt: "client-05" },
        { src: require("./assets/images/client-logo-06.png"), alt: "client-06" },
      ],
      coursesList: [
        { id: 1, title: 'Personal Finance: Financial Security Thinking & Principles', price: 'Free', lessons: '2', students: '201', thumb: require("./assets/images/finance-course-thumbnail-04-480x298.jpeg") },
        { id: 2, title: 'Learning to Write as a Professional Author', price: '$40.00', lessons: '20', students: '63', thumb: require("./assets/images/course-02-480x298 (1).jpeg") },
        { id: 3, title: 'Customer-centric Info-Tech Strategies', price: 'Free', lessons: '24', students: '885', thumb: require("./assets/images/stock-full-hd-03-480x298 (1).jpeg") },
        { id: 4, title: 'Master jQuery in a Short Period of Time', price: '$19.00', lessons: '17', students: '63', thumb: require("./assets/images/stock-full-hd-04-480x298 (1).jpeg") },
        { id: 5, title: 'Academic Listening and Note-taking', price: '$26.00', lessons: '14', students: '68', thumb: require("./assets/images/stock-full-hd-06-480x298 (1).jpeg") },
        { id: 6, title: 'Master jQuery in a Short Period of Time', price: '$39.00', lessons: '6', students: '51', thumb: require("./assets/images/course-featured-image-01-480x298 (1).jpeg") },
      ],
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
