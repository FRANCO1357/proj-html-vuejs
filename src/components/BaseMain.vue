<template>
    <div>
        <TheAllCourses :courses="courses"/>
        <TheBenefits :benefits="benefits"/>
        <TheTutorial/>
        <TheTestimonials :testimonials="testimonials"/>
        <TheGetStarted/>
        <TheCompanyData :brandData="brandData"/>
        <TheBlogsArticles :articles="blogsArticles"/>
        <TheSubscription/>
    </div>
</template>

<script>
import TheBenefits from './TheBenefits.vue';
import TheAllCourses from './TheAllCourses.vue';
import TheTutorial from './TheTutorial.vue';
import TheTestimonials from './TheTestimonials.vue';
import TheGetStarted from './TheGetStarted.vue';
import TheCompanyData from './TheCompanyData.vue';
import TheBlogsArticles from './TheBlogsArticles.vue';
import TheSubscription from './TheSubscription.vue';
    export default{
    name: "baseMain",
    components: {
    TheAllCourses,
    TheBenefits,
    TheTutorial,
    TheTestimonials,
    TheGetStarted,
    TheCompanyData,
    TheBlogsArticles,
    TheSubscription,
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