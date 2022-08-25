<template>
    <div class="company-data">
        <div class="container">
            <div v-for="data in brandData" :key="data.title" class="company-data-card">
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
@import "../assets/sass/vars";
.container{
    display: flex;
    padding: 0 20px;

    .company-data-card{
        width: 25%;
        text-align: center;
        padding: 80px 20px;
        border-left: 1px solid $dark_background;

        &:last-child{
           border-right: 1px solid $dark_background; 
        }

        h4{
            color: $title_color;
            font-size: 22px;
            font-weight: 600;
            padding: 0 40px;
            margin: 10px 0;
        }

        strong{
            font-size: 60px;
            color: $main_color;
        }

        h5{
            font-size: 18px;
            font-weight: 500;
            color: $title_text;
            margin-bottom: 20px;
        }
    }
}
</style>