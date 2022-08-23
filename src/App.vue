<template>
  <div>
    <BaseHeader :links="menuLinks"/>
    <TheJumbotron/>
    <BaseMain/>
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
        { text: "Menù", src: "#" },
        { text: "Pages", src: "#" },
        { text: "Courses", src: "#" },
        { text: "Features", src: "#" },
        { text: "Blog", src: "#" },
        { text: "Shop", src: "#" },
      ]
    }
  }
}
</script>

<style lang="scss">
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;

    body{
      font-family: 'Poppins', sans-serif;
      background-color: grey;

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
      width: 1100px;
      margin: 0 auto;
      padding: 20px;
    }
    }


  }
</style>
