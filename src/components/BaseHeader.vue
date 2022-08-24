<template>
    <header>
        <div class="container">
            <a href=""><img src="../assets/images/dark-logo.png" alt=""></a>
            <nav>
                <ul>
                    <li v-for="link in links" :key="link.text">
                        <a :href="link.href">{{link.text}}<i class="fa-solid fa-angle-down"></i></a>
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
                        font-size: 14px;

                        i{
                            margin-left: 5px;
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
                    position: relative;

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