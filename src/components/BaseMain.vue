<template>
    <div>
        <TheAllCourses :courses="courses"/>
        <TheBenefits :benefits="benefits"/>
        <TheTutorial/>
        <TheTestimonials :testimonials="testimonials"/>
        <TheGetStarted/>
        <TheBrandData :brandData="brandData"/>
        <TheBlogsArticles :articles="blogsArticles"/>
    </div>
</template>

<script>
import TheBenefits from './TheBenefits.vue';
import TheAllCourses from './TheAllCourses.vue';
import TheTutorial from './TheTutorial.vue';
import TheTestimonials from './TheTestimonials.vue';
import TheGetStarted from './TheGetStarted.vue';
import TheBrandData from './TheBrandData.vue';
import TheBlogsArticles from './TheBlogsArticles.vue';
    export default{
    name: "baseMain",
    components: {
    TheAllCourses,
    TheBenefits,
    TheTutorial,
    TheTestimonials,
    TheGetStarted,
    TheBrandData,
    TheBlogsArticles,
},
    props:{
        courses: Array,
        benefits: Array,
        testimonials: Array,
        brandData: Array,
        blogsArticles: Array,
    }
}
</script>

<style lang="scss" scoped>
</style>