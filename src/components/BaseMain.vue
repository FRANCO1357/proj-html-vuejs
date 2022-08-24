<template>
    <div>
        <TheAllCourses :courses="courses"/>
        <TheBenefits :benefits="benefits"/>
        <TheTutorial/>
        <TheTestimonials :testimonials="testimonials"/>
    </div>
</template>

<script>
import TheBenefits from './TheBenefits.vue';
import TheAllCourses from './TheAllCourses.vue';
import TheTutorial from './TheTutorial.vue';
import TheTestimonials from './TheTestimonials.vue';
    export default{
    name: "baseMain",
    components: {
    TheAllCourses,
    TheBenefits,
    TheTutorial,
    TheTestimonials
},
    props:{
        courses: Array,
        benefits: Array,
        testimonials: Array,
    }
}
</script>

<style lang="scss" scoped>
</style>