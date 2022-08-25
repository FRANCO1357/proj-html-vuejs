<template>
    <div class="blogs-articles">
        <div class="container">
            <div class="most-viewed">
                <p>ENJOYABLE INSIGHTS</p>
                <h3>Most Viewed <span>Best Blogs</span></h3>
                <a href=""><i class="fa-solid fa-arrow-right-long"></i> Become a Better Blogger: Content Planning</a>
                <a href=""><i class="fa-solid fa-arrow-right-long"></i> Promoting Your Online Business on Pinterest</a>
                <a href=""><i class="fa-solid fa-arrow-right-long"></i> Gamification and Game-Based Learning</a>
                <a href=""><i class="fa-solid fa-arrow-right-long"></i> Designing an Online Course from Expert’s Perspective</a>
                <a href=""><i class="fa-solid fa-arrow-right-long"></i> Why Online Courses Are the Future of Education</a>
            </div>
            <div v-for="article in articles" :key="article.title" class="blog-articles-card">
        <img :src="article.thumb" alt="">
        <div class="description">
            <p>{{article.topic}}</p>
            <h4>{{article.title}}</h4>
            <div class="info">
                <p><i class="fa-solid fa-calendar"></i> {{article.data}}</p>
                <p><i class="fa-solid fa-eye"></i> {{article.views}}</p>
            </div>
        </div>
    </div>

        </div>
    </div>
</template>

<script>
export default{
    name: "TheBlogsArticles",
    props: {
        articles: Array,
    },
}
</script>
    
<style lang="scss" scoped>
@import "../assets/sass/vars";
.blogs-articles{
    background-color: $dark_background;

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;

        .most-viewed{
            display: flex;
            flex-direction: column;
            width: 40%;
            margin: 20px;

            p{
                color: $title_text;
            }

            h3{
                color: $title_color;
                font-size: 32px;
                font-weight: 600;
                margin: 20px 0;

                span{
                    font-weight: 400;
                    color: $main_color;
                }
            }

            a{
                color: $title_color;
                text-decoration: none;
                font-size: 14px;
                font-weight: 500;
                margin: 10px 0;

                &:hover{
                    color: $main_color;
                }
            }
        }

        .blog-articles-card{
            cursor: pointer;
            background-color: white;
            width: 30%;
            margin: 25px;
            border-radius: 5px;
            box-shadow: 0 1px 6px rgb(206, 206, 206);

            img{
                border-radius: 5px 5px 0 0;
            }

            .description{
                padding: 20px;

                p{
                    color: $text_color;
                }

                h4{
                    color: $title_color;
                    margin: 10px 0;

                    &:hover{
                        color: $main_color;
                    }
                }

                .info{
                display: flex;
                margin: 10px 0;

                p{
                    margin-right: 30px;
                    font-size: 14px;
                    font-weight: 200;

                    i{
                        margin-right: 5px;
                    }
                }
            }
            }
        }
    }
}

</style>