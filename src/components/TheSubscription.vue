<template>
    <div class="subscription">
        <div class="container">
            <h3>Subscribe <span>Newsletters</span></h3>
            <p>Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
            <div class="form-field">
                <input type="email" placeholder="Enter your email">
                <a href="#">Subscribe</a>
            </div>
            <img class="background-image first" src="../assets/images/maxcoach-shape-02.png" alt="background-image-first">
            <img class="background-image second" src="../assets/images/maxcoach-circle-green.png" alt="background-image-second">
            <img class="background-image third" src="../assets/images/maxcoach-shape-09.png" alt="background-image-third">
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheSubscription'
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";
.subscription{
    text-align: center;
    padding: 50px;
    position: relative;

    h3{
        color: $title_color;
        font-size: 32px;
        font-weight: 600;

        span{
            font-weight: 400;
            color: $main_color;
        }
    }

    p{
        color: $text_color;
        width: 600px;
        margin: 20px auto;
    }

    .form-field{
        display: flex;
        justify-content: center;
        margin: 35px 0;

        input{
            height: 50px;
            width: 500px;
            padding: 20px 15px;
            border: none;
            border-radius: 5px 0 0 5px;
            background-color: $light_background;

            &::placeholder{
                color: grey;
                font-size: 14px;
                font-weight: 100;
            }

            &:focus-visible{
                background-color: white;
                border: 0.5px solid $main_color;
                font-weight: 100;
            }
        }

        a{
            display: inline-block;
            background-color: $main_color;
            height: 50px;
            width: 120px;
            text-decoration: none;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 0 5px 5px 0;
            font-size: 14px;

            &:hover{
                background-color: $button_hover;
                transition: 0.3s linear;
            }
        }
    }

    .background-image{
        border-radius: 0%;
        position: absolute;
                

        &.first{
            right: 80px;
            top: 180px;
        }

        &.second{
            width: 60px;
            left: 150px;
            top: 200px;
        }

        &.third{
            right: 200px;
            top: 40px;
        }
    }
}
</style>