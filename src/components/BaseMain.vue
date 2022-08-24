<template>
    <div>
        <TheAllCourses :courses="courses"/>
        <TheBenefits :benefits="benefits"/>
        <TheTutorial/>
    </div>
</template>

<script>
import TheBenefits from './TheBenefits.vue';
import TheAllCourses from './TheAllCourses.vue';
import TheTutorial from './TheTutorial.vue';
    export default{
    name: "baseMain",
    components: { 
        TheAllCourses,
        TheBenefits,
        TheTutorial,
        },
    props:{
        courses: Array,
        benefits: Array,
    }
}
</script>

<style lang="scss" scoped>
</style>