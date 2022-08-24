<template>
    <div class="jumbotron-bottom">
        <div v-for="icon in icons" :key="icon.alt" class="jumbotron-card">
            <img :src="icon.src" :alt="icon.alt">
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheJumbotronCard',
    props:{
        icons: Array
    }
}
</script>

<style lang="scss" scoped>
    .jumbotron-bottom{
        display: flex;
        justify-content: space-between;
        margin-top: 30px;

        .jumbotron-card{
            opacity: 0.5;

            &:hover{
                opacity: 1;
                transition: 0.5s linear;
            }
        }
    }
</style>