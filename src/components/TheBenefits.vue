<template>
    <div class="benefits">
        <div class="container">
            <p>MAXCOACH AVAILABLE COURSES</p>
            <h3>Access <span>Smart Tutoring</span> Program For Benefits.</h3>
            <TheBenefitCard :benefits="benefits"/>
        </div>
    </div>
</template>

<script>
import TheBenefitCard from './TheBenefitCard.vue';
export default{
    name: 'TheBenefits',
    components:{
    TheBenefitCard,
},
    props:{
        benefits: Array,
    }
}
</script>

<style lang="scss" scoped>
.benefits{
    text-align: center;

    p{
        color: grey;
        font-weight: 200;
        margin-top: 50px;
    }

    h3{
        font-size: 30px;
        font-weight: 600;

        span{
            font-weight: 300;
            color: green;
        }
    }
}
</style>