<template>
    <div class="brand-data">
        <div class="container">
            <div v-for="data in brandData" :key="data.title" class="brand-data-card">
                <h4>{{data.title}}</h4>
                <strong>{{data.number}}</strong>
                <h5>{{data.name}}</h5>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheBrandData',
    props:{
        brandData: Array,
    }
}
</script>

<style lang="scss" scoped>
.container{
    display: flex;
    padding: 0 20px;

    .brand-data-card{
        width: 25%;
        text-align: center;
        padding: 80px 20px;
        border-left: 1px solid rgb(234, 234, 234);

        &:last-child{
           border-right: 1px solid rgb(234, 234, 234); 
        }

        h4{
            font-size: 22px;
            font-weight: 600;
            padding: 0 40px;
            margin: 10px 0;
        }

        strong{
            font-size: 60px;
            color: green;
        }

        h5{
            font-size: 18px;
            font-weight: 500;
            color: grey;
        }
    }
}
</style>