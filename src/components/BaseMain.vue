<template>
    <div>
        <TheAllCourses :courses="courses"/>
        <TheBenefits :benefits="benefits"/>
    </div>
</template>

<script>
import TheBenefits from './TheBenefits.vue';
import TheAllCourses from './TheAllCourses.vue';
    export default{
    name: "baseMain",
    components: { 
        TheAllCourses,
        TheBenefits,
        },
    props:{
        courses: Array,
        benefits: Array,
    }
}
</script>

<style lang="scss" scoped>
</style>