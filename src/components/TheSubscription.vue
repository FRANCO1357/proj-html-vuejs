<template>
    <div class="subscription">
        <div class="container">
            <h3>Subscribe <span>Newsletters</span></h3>
            <p>Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
            <div class="form-field">
                <input type="email" placeholder="Enter your email">
                <a href="">Subscribe</a>
            </div>
            <img class="background-image first" src="../assets/images/maxcoach-shape-02.png" alt="">
            <img class="background-image second" src="../assets/images/maxcoach-circle-green.png" alt="">
            <img class="background-image third" src="../assets/images/maxcoach-shape-09.png" alt="">
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheSubscription'
}
</script>

<style lang="scss" scoped>
.subscription{
    text-align: center;
    padding: 50px;
    position: relative;

    h3{
        font-size: 32px;
        font-weight: 600;

        span{
            font-weight: 400;
            color: green;
        }
    }

    p{
        color: grey;
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
            background-color: rgb(233, 233, 233);

            &::placeholder{
                color: grey;
                font-size: 14px;
                font-weight: 100;
            }

            &:focus-visible{
                background-color: white;
                border: 0.5px solid green;
                font-weight: 100;
            }
        }

        a{
            display: inline-block;
            background-color: green;
            height: 50px;
            width: 120px;
            text-decoration: none;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 0 5px 5px 0;
            font-size: 14px;
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