<template>
    <div class="tutorial">
        <div class="container">
            <div class="video-tutorial">
                <img src="../assets/images/icon-youtube-play.png" alt="">
                <img class="background-image first" src="../assets/images/maxcoach-shape-05-150x150.png" alt="">
                <img class="background-image second" src="../assets/images/maxcoach-shape-07.png" alt="">
                <img class="background-image third" src="../assets/images/maxcoach-shape-02.png" alt="">
            </div>
            <div class="description">
                <p>GET STARTED <strong>EFFORTLESSLY</strong></p>
                <h3>Enjoy Our <span>Companionship</span></h3>
                <p>Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for some hidden hints of early-bird rewards as well.</p>
                <a href="#">Download free guidebook <i class="fa-solid fa-arrow-right-long"></i></a>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheTutorial',
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";
.container{
    display: flex;
    padding: 100px 0;

    .video-tutorial{
        width: 55%;
        height: 420px;
        border-radius: 5px;
        background-image: url('../assets/images/home-2-popup-video-poster.jpg');
        background-repeat: no-repeat;
        background-size: 100%;
        background-position: center;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: 0.5s linear;
        position: relative;   

        &:hover{
            background-size: 110%;
            
        }

        .background-image{
                z-index: -1;
                position: absolute;
                

                &.first{
                    left: -70px;
                    top: 80px;
                }

                &.second{
                    right: -20px;
                    top: 350px;
                }

                &.third{
                    right: -140px;
                    top: -100px;
                }

            }
    }

    .description{
        width: 45%;
        padding: 40px 0 80px 80px;

        h3{
            color: $title_color;
            font-size: 42px;
            font-weight: 600;
            margin: 20px 0;

            span{
                font-weight: 300;
                color: $main_color;
            }
        }

        p{
            color: $text_color;
            font-size: 18px;
            font-weight: 200;

            strong{
                color: $title_color;
            }
        }

        a{
            display: block;
            color: $main_color;
            font-weight: 500;
            font-size: 14px;
            margin-top: 30px;
            text-decoration: none;
        }
    }

}
</style>