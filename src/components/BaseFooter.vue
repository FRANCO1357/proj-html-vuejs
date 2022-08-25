<template>
<footer>
    <div class="container">
        <div class="company-info">
            <h4>Address</h4>
            <p>382 NE 191st St # 87394 Miami, FL 33179-3899</p>
            <p>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</p>
            <a href="#">support@maxcoach.com</a>
            <div class="social-icons">
                <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
                <a href="#"><i class="fa-brands fa-linkedin"></i></a>            
            </div>
        </div>
        <TheFooterMenuCard :footerMenuLinks="footerMenuLinks"/>
    </div>
    <p>© 2020 Maxcoach. All Rights Reserved</p>
</footer>
</template>

<script>
import TheFooterMenuCard from './TheFooterMenuCard.vue';
export default{
    name: 'BaseFooter',
    components:{
        TheFooterMenuCard,
    },
    props:{
        footerMenuLinks: Array,
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";
footer{
    background-color: $light_background;
    color: $text_color;
    font-weight: 200;
    font-size: 14px;
    padding: 50px;

    a{
        display: inline-block;
        text-decoration: none;
        color: $text_color;
        margin-bottom: 10px;

        &:hover{
            color: $main_color;
            transition: 0.5s linear;
            }
        }


    .container{
        display: flex;  

        h4{
            color: black;
            font-size: 18px;
            font-weight: 500;
            margin-bottom: 20px;
        }

        .company-info{
            width: 50%;

            p{
                margin-bottom: 10px;
                margin-top: 0;
                text-align: left;
            }

            .social-icons{
                margin-top: 30px;

                i{
                font-size: 26px;
                margin-right: 30px;
                
                &:hover{
                    color: $main_color;
                    transition: 0.5s linear;
                }
            }

            }
            
        }

    }

    p{
        text-align: center;
        margin-top: 50px;
    }
}

</style>