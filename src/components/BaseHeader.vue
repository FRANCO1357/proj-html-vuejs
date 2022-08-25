<template>
    <header>
        <div class="container">
            <a href=""><img src="../assets/images/dark-logo.png" alt="logo"></a>
            <nav>
                <ul>
                    <li v-for="link in links" :key="link.text">
                        <a :href="link.href">{{link.text}}<i class="fa-solid fa-angle-down"></i></a>
                        <div class="sub-menu">
                            <a v-for="link in link.link" :key="link.text" :href="link.href">{{link}}</a>
                        </div>
                    </li>
                </ul>
                <div class="search-field">
                    <input type="text" placeholder="Search...">
                    <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
                </div>
            </nav>
        </div>
    </header>
</template>

<script>
    export default{
        name: 'baseHeader',
        props:{
            links: Array,
        }
    }
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

    header{
        background-color: white;
        box-shadow: 0 0.2px 8px rgb(218, 218, 218);

        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;

            a{
                width: 150px;
                color: black;

                &:hover{
                    color: $main_color;
                }
            }

            nav{
                display: flex;
                align-items: center;
                height: 80px;

                ul{
                    display: flex;
                    align-items: center;
                    height: 100%;

                    li{
                        position: relative;
                        height: 100%;
                        margin-top: 55px;

                        &:hover .sub-menu{
                            display: flex;
                            flex-direction: column;
                        }

                        .sub-menu{
                            z-index: 1;
                            position: absolute;
                            top: 52px;
                            left: 0;
                            width: 250px;
                            min-height: 10px;
                            background-color: white;
                            box-shadow: 0 1px 6px rgb(216, 216, 216);
                            border-bottom: 4px solid $main_color;
                            display: none;
                            padding: 20px;

                            a{
                                margin: 5px 0;
                                color: $text_color;
                                font-weight: 200;

                                &:hover{
                                    color: black;
                                    transition: 0.5s linear;
                                }
                            }
                        }

                    a{
                        margin: 0 20px;
                        font-size: 14px;

                        i{
                            margin-left: 5px;
                        }
                    }

                    }       
                }

                .search-field{
                    display: flex;

                    input{
                        margin-left: 20px;
                        height: 30px;
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
                            border: 0.5px solid $main_color;
                            font-weight: 100;
                        }
                    }

                    a{
                        display: inline-block;
                        color: $main_color;
                        text-decoration: none;
                        background-color: rgb(233, 233, 233);
                        width: 50px;
                        height: 40px;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        border-radius: 0 5px 5px 0;

                        &:hover{
                            background-color: $main_color;
                            color: white;
                            transition: 0.3s linear;
                        }
                    }

                }
            }
        }
    }
</style>