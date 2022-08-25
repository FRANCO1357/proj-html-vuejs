<template>
    <div class="all-courses">
        <div class="container">
            <p>SIMULATED TO LEARN?</p>
            <h3>Featured online courses</h3>
                <TheCourseCard :courses="courses" />
            <a href="#">View all courses <i class="fa-solid fa-arrow-right-long"></i></a>
        </div>
    </div>
</template>

<script>
import TheCourseCard from './TheCourseCard.vue';
export default{
    name: 'TheAllCourses',
    components: {
    TheCourseCard,
},
    props:{
        courses: Array,
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";
.all-courses{
    background-color: $light_background;
    text-align: center;
    padding: 50px 0;

    p{
        color: grey;
        font-weight: 200;
    }

    h3{
        font-size: 30px;
        font-weight: 600;
    }
    
    a{
        display: inline-block;
        background-color: $main_color;
        border-radius: 5px;
        padding: 15px 60px;
        margin: 15px 0;
        color: white;
        font-size: 14px;
        font-weight: 500;

        &:hover{
            background-color: $button_hover;
            transition: 0.3s linear;
        }
    }
}
</style>