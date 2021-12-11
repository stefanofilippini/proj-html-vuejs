<template>
    <div class="background-image">
        <div class="background-container">
            <header>
                <a href="#">
                    <img class="logo" src="@/assets/theme_eduprime_logo.png" alt="LOGO">
                </a>
                <nav>
                    <ul>
                        <li v-for="(item, i) in navList" :key="`item-${i}`">
                            <a href="#">{{item.name}} <span v-show="item.Menu === true"><i class="fas fa-caret-down"></i></span></a>
                        </li>
                    </ul>
                </nav>
            </header>
            <section class="hero">
                <h2>Key to your success</h2>
                <div>
                    EduPrime is the most versatile WordPress theme for educational pourposes,<br>
                    showcasing universities, courses, secondary schools etc.
                </div>
                <div class="buttons">
                    <a class="button-1" href="#"><i class="fas fa-search"></i> Search courses</a>
                    <a class="button-1" href="#"><i class="fas fa-user-plus"></i> Apply for universities</a>
                </div>
            </section>
            <img class="wave-1" preserveAspectRatio="none" src="@/assets/svg/wave-1.svg" alt="">
            <img class="wave-1" preserveAspectRatio="none" src="@/assets/svg/wave-2.svg" alt="">
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'Header',

    data() {
        return {
            navList: [
                {
                    name: 'Home',
                    Menu: true,
                },
                {
                    name: 'Courses',
                    Menu: true,
                },
                {
                    name: 'About Us',
                    Menu: false,
                },
                {
                    name: 'News',
                    Menu: true,
                },
                {
                    name: 'Pages',
                    Menu: true,
                },
                {
                    name: 'Contact',
                    Menu: false,
                },
                {
                    name: 'Purchase',
                    Menu: false,
                },
                {
                    name: 'View courses',
                    Menu: false,
                },
            ]
        }
    }

}
</script>

<style scoped lang="scss">
    .background-image {
        height: 800px;
        background-image: url(../assets/theme_slider2_bg-1.jpg);
        .background-container {
            position: relative;
            width: 100%;
            height: 100%;
            background-color: rgba($color: #df5e60, $alpha: 0.9);
            header {
                display: flex;
                align-items: center;
                justify-content: space-between;
                height: 200px;
                padding: 60px;
                a {
                    .logo {
                        height: 75px;
                    }
                }
                nav {
                    ul {
                        list-style: none;
                        display: flex;
                        align-items: center;
                        li {
                            margin-right: 30px;
                            font-size: 17px;
                            color: white;
                            &:hover {
                                a {
                                    color: #e9d758;
                                }
                            }
                            a {
                                color: white;
                                text-decoration: none;
                                span {
                                    margin-left: 3px;
                                    font-size: 12px;
                                }
                            }
                            &:last-of-type {
                                background-color: #e5d45d;
                                text-transform: uppercase;
                                padding: 25px 40px;
                                border-radius: 100px;
                                &:hover {
                                    background-color: white;
                                    a {
                                        color: #df5e60;
                                    }
                                }
                            }
                        }
                    }
                }
            }
            .hero {
                margin-top: 30px;
                display: flex;
                flex-direction: column;
                align-items: center;
                color: white;
                h2 {
                    font-size: 60px;
                }
                div {
                    margin-top: 30px;
                    text-align: center;
                    font-size: 20px;
                    font-family: sans-serif;
                    line-height: 35px;
                }
                .buttons {
                    margin-top: 70px;
                    a {
                        text-decoration: none;
                        padding: 25px 40px;
                        border-radius: 100px;
                        font-size: 16px;
                        &:first-of-type {
                            margin-right: 30px;
                        }
                    }
                }
            }
            .wave-1 {
                position: absolute;
                bottom: -1px;
                left: 0;
                width: 100%;
                height: 100px;
                color: white;
            }
        }
    }

</style>