<template>
    <div class="courses">
        <div v-for="course in courses" :key="course.id" class="course-card">
            <div class="thumb">
                <img :src="course.thumb" :alt="course.title">
            </div>
            <div class="description">
                <h4>{{course.price}}</h4>
                <h5>{{course.title}}</h5>
                <div class="course-data">
                    <p><i class="fa-regular fa-file-lines"></i> {{course.lessons}} Lessons</p>
                    <p><i class="fa-solid fa-user-large"></i> {{course.students}} Students</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'TheCourseCard',
    props:{
        courses: Array,
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";
.courses{
    margin-top: 40px;
    display: flex;
    flex-wrap: wrap;
    width: 100%;

    .course-card{
        cursor: pointer;
        width: 50%;
        height: 202px;
        text-align: left;
        display: flex;
        margin: 10px 0;
        padding: 15px;
        border-radius: 6px;

        &:hover{
            background-color: white;
            box-shadow: 0 0.5px 5px rgb(227, 227, 227);
            transition: 0.5s linear;
        }

        .thumb {

            width: 35%;

            img{
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
        }
        }
        
        .description{
            width: 65%;
            display: flex;
            flex-direction: column;
            justify-content: space-around;
            margin: 30px;

            h4{
                color: $main_color;
                font-size: 24px;
            }

            h5{
                font-size: 20px;
                font-weight: 500;
                margin-bottom: 10px;
                color: $title_color;
            }
        }

        .course-data{
            display: flex;
            
            p{
                margin-right: 50px;
                color: $title_text;
                font-size: 14px;
                font-weight: 100;
            }
        }

    }
}
</style>