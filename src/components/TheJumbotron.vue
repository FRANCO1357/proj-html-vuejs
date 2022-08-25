<template>
    <div class="jumbotron">
        <div class="container">
            <div class="jumbotron-top">
                <div class="description">
                    <h2>Distant learning for further expansion</h2>
                    <p>Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process.</p>
                    <a class="button" href=""><i class="fa-solid fa-download"></i> Download free guide</a>
                    <div class="sample">
                        <p>Have questions?</p><a href="">Get free semple <i class="fa-solid fa-arrow-right-long"></i></a>
                    </div>
                </div>
                <figure>
                    <img src="../assets/images/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg" alt="">
                    <img class="background-image first" src="../assets/images/maxcoach-shape-08.png" alt="">
                    <img class="background-image second" src="../assets/images/maxcoach-shape-08.png" alt="">
                    <img class="background-image third" src="../assets/images/maxcoach-shape-07.png" alt="">
                    <img class="background-image fourth" src="../assets/images/maxcoach-shape-02.png" alt="">
                </figure>
            </div>
            <TheJumbotronCard :icons="icons"/>
        </div>
    </div>
</template>

<script>
import TheJumbotronCard from './TheJumbotronCard.vue';
export default{
    name: "TheJumbotron",
    props: {
        icons: Array,
    },
    components: { TheJumbotronCard }
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";
.container{

    a{
        text-decoration: none;
        color: $main_color;
    }

    .jumbotron-top{
        display: flex;
        align-items: center;

        .description{
            width: 45%;
            padding-right: 50px;

            h2{
                color: $title_color;
                font-size: 40px;
                font-weight: 600;
                margin: 10px 0;
            }

            p{
                color: $title_text;
            }

            .button{
                display: inline-block;
                background-color: $main_color;
                border-radius: 5px;
                padding: 15px 50px;
                margin: 15px 0;
                color: white;
                font-size: 12px;
                font-weight: 500;

                &:hover{
                    background-color: $button_hover;
                    transition: 0.3s linear;
                }
            }

            .sample{
            display: flex;
            font-size: 14px;

            p{
                font-size: 14px;
                margin-right: 10px;
            }

            a{
                font-weight: 500;
                border-bottom: 0.5px solid grey;
            }
        }
        }

        figure{
            width: 55%;
            padding: 50px;
            position: relative;   

            img{
            border-radius: 100%;
            }

            .background-image{
                z-index: -1;
                border-radius: 0%;
                position: absolute;
                

                &.first{
                    left: 0;
                    top: 150px;
                }

                &.second{
                    left: 0;
                    top: 300px;
                }

                &.third{
                    right: 100px;
                    top: 410px;
                }

                &.fourth{
                    right: -50px;
                    top: 100px;
                }

            }
        }        
    }
}
</style>