<template>
    <div class="get-started">
        <div class="container">
            <h4>Start today for getting <span>Online Certification</span></h4>
            <h3>You can be your own guiding star with our help!</h3>
            <a href="#">Get started now</a>
        </div>
        <img class="background-image first" src="../assets/images/maxcoach-shape-02.png" alt="">
        <img class="background-image second" src="../assets/images/maxcoach-circle.png" alt="">
        <img class="background-image third" src="../assets/images/maxcoach-shape-01.png" alt="">
    </div>
</template>

<script>
export default{
    name: 'TheGetStarted',
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";
.get-started{
    background-color: $light_background;
    text-align: center;
    position: relative;

    h4{
        color: $title_color;
        font-size: 22px;
        font-weight: 600;

        span{
            color: $main_color;
            font-weight: 300;
        }
    }

    h3{
        color: $title_color;
        font-size: 32px;
        font-weight: 600;
    }

    a{
        display: inline-block;
        background-color: $main_color;
        border-radius: 5px;
        padding: 15px 60px;
        margin: 50px 0;
        color: white;
        font-size: 14px;
        font-weight: 500;
        text-decoration: none;

        &:hover{
            background-color: $button_hover;
            transition: 0.3s linear;
        }
    }

    .background-image{
                border-radius: 0%;
                position: absolute;
                

                &.first{
                    right: 100px;
                    top: 50px;
                }

                &.second{
                    width: 60px;
                    left: 120px;
                    top: 20px;
                }

                &.third{
                    left: 150px;
                    top: 80px;
                }
    }
}
</style>