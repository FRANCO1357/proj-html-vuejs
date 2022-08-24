<template>
    <div class="testimonials">
        <div class="container">
            <p>GREAT WORDS ABOUT MAXCOACH</p>
            <h3>Our <span>top learners'</span> verbatim</h3>
            <div class="testimonials-list">
                <div v-for="testimonial in testimonials" :key="testimonial.name" class="testimonial-card">
                    <h4>{{testimonial.title}}</h4>
                    <p>{{testimonial.text}}</p>
                    <div class="testimonial-info">
                        <img :src="testimonial.thumb" alt="">
                        <div class="text">
                            <p>{{testimonial.name}}</p>
                            <p>{{testimonial.position}}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="selector">
                <i v-for="testimonial in testimonials" :key="testimonial.name" class="fa-solid fa-circle"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheTestimonials',
    props:{
        testimonials: Array,
    }
}
</script>

<style lang="scss" scoped>
.testimonials{
    background-color: rgb(234, 234, 234);
    text-align: center;


    p{
        color: grey;
        font-weight: 200;
        margin-top: 50px;
    }

    h3{
        font-size: 30px;
        font-weight: 600;

        span{
            font-weight: 300;
            color: green;
        }
    }

    .testimonials-list{
        display: flex;
        margin-top: 50px;

        .testimonial-card{
            background-color: white;
            margin: 10px;
            padding: 30px;
            border-radius: 5px;

            h4{
                font-weight: 600;
                font-size: 14px;
            }

            p{
                margin-top: 15px;
                font-size: 12px;
            }

            .testimonial-info{
                display: flex;
                align-items: center;
                margin-top: 20px;

                img{
                    width: 80px;
                    height: 80px;
                    border-radius: 100%;
                }

                .text{
                    display: flex;
                    flex-direction: column;

                    text-align: left;
                    margin-left: 10px;
                }
            }
        }
    }

    .selector{

        i{
            font-size: 10px;
            margin: 50px 10px;
        }
    }
}
</style>