<template>
    <div class="background-container">
        <div class="container">
            <div class="left-footer">
                <img src="@/assets/theme_eduprime_logo.png" alt="">
                <p>
                    EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.
                </p>
                <ul>
                    <li v-for="(social, i) in Socials" :key="`social-${i}`">
                        <a href="#"><i class="fab" :class="social"></i></a>
                    </li>
                </ul>
            </div>
            <div class="list">
                <h5>Get EduPrime</h5>
                <ul>
                    <li v-for="(link, i) in Links1" :key="`link-${i}`">
                        <a href="#">{{ link }}</a>
                    </li>
                </ul>
            </div>
            <div class="list">
                <h5>Networking</h5>
                <ul>
                    <li v-for="(link, i) in Links2" :key="`link-${i}`">
                        <a href="#">{{ link }}</a>
                    </li>
                </ul>
            </div>
            <div class="right-footer">
                <div class="form">
                        <input type="text" placeholder="Search ...">
                        <button><i class="fas fa-search"></i></button>
                </div>
                <h5>Search Categories</h5>
                <ul>
                    <li v-for="(category, i) in Categories" :key="`category-${i}`">
                        <a href="#">{{ category }}</a>
                    </li>
                </ul>
                <div class="copyright">
                    ModelTheme. All rights reserved.
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer',

    data() {
        return {
            Socials: [
                'fa-facebook-f',
                'fa-twitter',
                'fa-instagram',
            ],

            Links1: [
                'Request a website',
                'Browse Themes',
                'Payment options',
                'Support System',
                'Checkout',
                'Purchase Theme'
            ],

            Links2: [
                'Purchase Theme',
                'Our Benefits',
                'Our Team',
                'Our Services',
                'Other Products',
                'My account'
            ],

            Categories: [
                'Business',
                'Coaching',
                'Design',
                'Economy',
                'Fitness',
                'Law',
                'Medicine',
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '@/styles/Global.scss';
    .background-container {
        background-color: $primary_color;
        height: 500px;
        display: flex;
        justify-content: center;
        .container {
            width: 70%;
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            .left-footer {
                width: 28%;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: start;
                color: white;
                img {
                    height: 70px;
                    margin-bottom: 50px;
                }
                p {
                    font-family: sans-serif;
                    margin-bottom: 35px;
                }
                ul {
                    list-style: none;
                    display: flex;
                    li {
                        height: 50px;
                        width: 50px;
                        padding: 16px;
                        border: 2px solid $secondary_color;
                        border-radius: 50%;
                        margin-right: 15px;
                        transition: 0.5s;
                        a {
                            color: white;
                        }
                        &:hover {
                            background-color: $secondary_color;
                        }
                    }
                }
            }
            .list {
                color: white;
                h5 {
                    font-size: 25px;
                    margin-bottom: 30px;
                }
                ul {
                    list-style: none;
                    li {
                        margin-bottom: 15px;
                        a {
                            text-decoration: none;
                            color: white;
                            font-family: sans-serif;
                            font-size: 15px;
                            transition: 0.5s;
                            &:hover {
                                color: #e9d758;
                            }
                        }
                    }
                }
            }
            .right-footer {
                display: flex;
                flex-direction: column;
                align-items: end;
                color: white;
                width: 30%;
                .form {
                    position: relative;
                    margin-bottom: 30px;
                    input {
                        height: 75px;
                        width: 360px;
                        padding: 30px;
                        font-family: sans-serif;
                        font-size: 15px;
                        font-weight: 500;
                        border-radius: 100px;
                        border: none;
                    }
                    button {
                        position: absolute;
                        height: 75px;
                        width: 75px;
                        background-color: #e5d45d;
                        border-radius: 50%;
                        border: none;
                        color: white;
                        font-size: 20px;
                        right: 0px;
                        bottom: 0px;
                        cursor: pointer;
                        transition: 0.5s;
                        &:hover {
                            background-color: #dd3333;
                        }
                    }
                }
                h5 {
                    font-size: 17px;
                    margin-bottom: 20px;
                }
                ul {
                    list-style: none;
                    display: flex;
                    flex-direction: row-reverse;
                    flex-wrap: wrap;
                    margin-bottom: 20px;
                    li {
                        padding: 6px 14px;
                        border: 1px solid white;
                        border-radius: 50px;
                        margin-bottom: 10px;
                        margin-left: 10px;
                        transition: 0.5s;
                        a {
                            font-size: 11px;
                            font-family: sans-serif;
                            text-decoration: none;
                            color: white;
                            text-transform: uppercase;
                        }
                        &:hover {
                            border: 1px solid #e9d758;
                            background-color: #e9d758;
                        }
                    }
                }
                .copyright {
                    color: #e9d059;
                    font-family: sans-serif;
                    font-size: 15px;
                }
            }
        }
    }
</style>