<template>
    <div class="container">
        <div v-for="data in brandData" :key="data.title" class="brand-data-card">
            <h4>{{data.title}}</h4>
            <strong>{{data.number}}</strong>
            <h5>{{data.name}}</h5>
        </div>
    </div>
    
</template>

<script>
export default{
    name: 'TheBrandDataCard'
}
</script>

<style lang="scss" scoped></style>