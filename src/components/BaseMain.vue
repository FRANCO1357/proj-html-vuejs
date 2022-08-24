<template>
    <div>
        <TheAllCourses :courses="courses"/>
    </div>
</template>

<script>
import TheAllCourses from './TheAllCourses.vue';
    export default{
    name: "baseMain",
    components: { TheAllCourses },
    props:{
        courses: Array,
    }
}
</script>

<style lang="scss" scoped>
</style>