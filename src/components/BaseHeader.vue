<template>
    <header>
        <div class="container">
            <a href=""><img src="../assets/images/dark-logo.png" alt=""></a>
            <nav>
                <ul>
                    <li v-for="link in links" :key="link.text">
                        <a :href="link.src">{{link.text}}<i class="fa-solid fa-angle-down"></i></a>
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

        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;

            a{
                width: 150px;
            }

            nav{
                height: 20px;
                display: flex;
                align-items: center;

                ul{
                    display: flex;

                    a{
                        margin: 0 10px;
                        font-size: 12px;

                        i{
                            margin-left: 5px;
                        }
                    }
                }

                input{
                    margin-left: 20px;
                    height: 30px;
                    padding: 5px;
                    border: none;
                    border-radius: 5px;
                    background-color: grey;
                    position: relative;

                    &::placeholder{
                        color: black;
                        font-size: 12px;
                    }

                    &:focus-visible{
                        background-color: white;
                        border: 0.5px solid green;
                    }
                }
            }
        }
    }
</style>