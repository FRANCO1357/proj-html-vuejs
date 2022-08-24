<template>
    <div class="all-benefits">
        <div v-for="benefit in benefits" :key="benefit.title" class="benefits-card">
            <img :src="benefit.thumb" alt="">
            <h5>{{benefit.title}}</h5>
            <p>{{benefit.description}}</p>
            <a href="#">{{benefit.link}} <i class="fa-solid fa-arrow-right-long"></i></a>
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheBenefitCard',
    props:{
        benefits: Array,
    }
}
</script>

<style lang="scss" scoped>
.all-benefits{
    display: flex;
    margin: 50px 0;
    text-align: left;

    .benefits-card{
        padding-right: 40px;

        h5{
            font-size: 22px;
            font-weight: 500;
            margin: 15px 0;
        }

        p{
            color: grey;
            font-size: 14px;
            font-weight: 200;
            margin-bottom: 15px;
        }

        a{
            font-size: 14px;
            color: grey;
            text-decoration: none;
            font-weight: 500;
        }
    }
}
</style>