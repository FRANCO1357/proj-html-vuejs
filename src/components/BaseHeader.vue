<template>
    <header>
        <div class="container">
            <a href=""><img src="../assets/images/dark-logo.png" alt=""></a>
            <nav>
                <ul>
                    <li v-for="link in links" :key="link.text">
                        <a :href="link.href">{{link.text}}<i class="fa-solid fa-angle-down"></i></a>
                        <div class="sub-menu">
                            <a v-for="link in link.link" :key="link.text" href="#">{{link}}</a>
                        </div>
                    </li>
                </ul>
                <input type="text" placeholder="Search...">
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
                            border-bottom: 4px solid green;
                            display: none;
                            padding: 20px;

                            a{
                                margin: 5px 0;
                                color: grey;
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

                input{
                    margin-left: 20px;
                    height: 30px;
                    padding: 20px 15px;
                    border: none;
                    border-radius: 5px;
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
            }
        }
    }
</style>