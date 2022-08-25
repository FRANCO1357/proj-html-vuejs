<template>
<nav>
    <div v-for="link in footerMenuLinks" :key="link.text" class="footer-menu">
        <h4>{{link.text}}</h4>
        <ul>
            <li v-for="link in link.link" :key="link">
                <a href="#">{{link}}</a>
            </li>
        </ul>
    </div>
</nav>
</template>

<script>
export default{
    name: 'TheFooterMenuCard',
    props:{
        footerMenuLinks: Array,
    }
}
</script>

<style lang="scss" scoped>
nav{
    display: flex;
    width: 50%;

    .footer-menu{
            width: 50%;
        }

        h4{
            color: black;
            font-size: 18px;
            font-weight: 500;
            margin-bottom: 20px;
        }

        a{
        display: inline-block;
        text-decoration: none;
        color: grey;
        margin-bottom: 10px;

        &:hover{
            color: green;
            transition: 0.5s linear;
            }
        }
}
</style>