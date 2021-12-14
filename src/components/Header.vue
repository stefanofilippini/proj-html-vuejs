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
                    <a class="button-2" href="#"><i class="fas fa-user-plus"></i> Apply for universities</a>
                </div>
            </section>
            <svg class="wave-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="white" fill-opacity="0.9" d="M0,32L48,53.3C96,75,192,117,288,117.3C384,117,480,75,576,69.3C672,64,768,96,864,112C960,128,1056,128,1152,112C1248,96,1344,64,1392,48L1440,32L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>
            <svg class="wave-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="white" fill-opacity="0.9" d="M0,64L48,64C96,64,192,64,288,90.7C384,117,480,171,576,181.3C672,192,768,160,864,133.3C960,107,1056,85,1152,64C1248,43,1344,21,1392,10.7L1440,0L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>
            <!-- <img class="wave-1" preserveAspectRatio="none" src="@/assets/svg/wave-1.svg" alt="">
            <img class="wave-1" preserveAspectRatio="none" src="@/assets/svg/wave-2.svg" alt=""> -->
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
    @import '@/styles/Global.scss';
    .background-image {
        height: 800px;
        background-image: url(../assets/theme_slider2_bg-1.jpg);
        .background-container {
            position: relative;
            width: 100%;
            height: 100%;
            background-color: rgba($color: $primary_color, $alpha: 0.9);
            overflow-y: hidden;
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
                                    color: $secondary_color;
                                }
                            }
                            a {
                                color: white;
                                text-decoration: none;
                                transition: 0.5s;
                                span {
                                    margin-left: 3px;
                                    font-size: 12px;
                                }
                            }
                            &:last-of-type {
                                background-color: $secondary_color;
                                text-transform: uppercase;
                                padding: 25px 40px;
                                border-radius: 100px;
                                transition: 0.5s;
                                &:hover {
                                    background-color: white;
                                    a {
                                        color: $primary_color;
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
                bottom: -180px;
                left: 0;
                width: 100%;
                color: white;
            }
        }
    }

</style>