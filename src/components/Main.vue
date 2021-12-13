<template>
    <div class="container">
        <div class="background-image">
            <Section
                titleImage="Books-icon.png"
                title="Thousands of courses for any type of student"
                Paragraph="At EduPrime, it doesn't matter what domain you wishto pursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides."
                Button="Browse through courses"
                image="Graduation-Illustration.png"
            />
        </div>
        <section class="faculties">
            <h3>Faculties available at EduPrime</h3>
            <p>
                A single university with a load of courses, tailored<br>
                to satisfy any student's needs.
            </p>
            <ul>
                <li v-for="(facultie, i) in Faculties" :key="`facultie-${i}`">
                    <img :src="require(`../assets/${facultie.img}`)" alt="">
                    <h4>{{facultie.name}}</h4>
                </li>
            </ul>
            <div class="active-facultie">
                <img src="../assets/Gavel-Illustration-e1556884768193.png" alt="">
                <div class="description">
                    <h4>
                        Titolo
                    </h4>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe unde quae veniam doloremque facilis dolore recusandae consectetur sunt nemo vitae, commodi perferendis voluptatum reprehenderit tempore quas quos totam minima. Nemo?
                    </p>
                    <div class="buttons">
                        <a href="#" class="button-4">Read More</a>
                    </div>
                </div>
            </div>
        </section>
        <img class="upper-wave" src="../assets/svg/svg-0.svg" alt="">
        <section class="university-year">
            <img class="top-img" src="../assets/Clock-and-Bell.png" alt="">
            <h3>University Year</h3>
            <div class="timeline">
                <img src="../assets/Timeline-Item.png" alt="">
                <div v-for="(timeDot, i) in TimeDots" :key="`timeDot-${i}`" class="times-dots">
                    <div class="times-dot-title">
                        {{ timeDot.title }}
                    </div>
                    <div class="time-dot-description">
                        {{ timeDot.description }}
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import Section from '@/components/Section.vue'

export default {
    name: 'Main',
    
    data() {
        return {
            Faculties:[
                {
                    img: 'Gavel-v2.png',
                    name: 'Law Faculty',
                },
                {
                    img: 'Coins-tabs-v2.png',
                    name: 'Economy',
                },
                {
                    img: 'Medicine-tabs-v2.png',
                    name: 'Medicine',
                },
                {
                    img: 'Computer-tabs-v2.png',
                    name: 'Computer Science',
                },
                {
                    img: 'Palette-tabs-v2.png',
                    name: 'Graphic Design',
                },
            ],

            TimeDots: [
                {
                    title: "Orientation",
                    description: "First day of the university year, all student gather for the opening ceremony and then network with others"
                },
                {
                    title: "Demo Classes",
                    description: "In the first week, students try to accomodate with the teaching style and choose their optional courses"
                },
                {
                    title: "Evaluation",
                    description: "At the end of a semester, students take a general evaluation test for every subject they're learning"
                },
                {
                    title: "Graduation Day",
                    description: "On the day of graduation, all student gather for the ceremony and then network and party among others"
                },
            ]
        }
    },

    components: {
        Section,
    },

}
</script>

<style lang="scss" scoped>
    .container {
        overflow-x: hidden;
    }

    .background-image {
        height: 700px;
        background-image: url(../assets/home-background.png);
        background-repeat: no-repeat;
        background-position: center;
    }

    .faculties {
        color: #3d404f;
        display: flex;
        flex-direction: column;
        align-items: center;
        h3 {
            margin-top: 80px;
            font-size: 50px;
        }
        p {
            margin-top: 25px;
            text-align: center;
            font-family: sans-serif;
            line-height: 25px;
        }
        ul {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            list-style: none;
            height: 200px;
            width: 100%;
            background-color: white;
            box-shadow: rgba(17, 17, 26, 0.1) 0px 4px 16px, rgba(17, 17, 26, 0.05) 0px 8px 32px;
            li {
                padding: 30px;
                border: 1px solid #eaeaea;
                width: 250px;
                display: flex;
                flex-direction: column;
                align-items: center;
                color: #e56768;
                img {
                    height: 100%;
                    margin-bottom: 20px;
                }
            }
        }
        .active-facultie {
            width: 60%;
            display: flex;
            justify-content: center;
            align-items: center;
            img {
                padding: 80px;
                width: 50%;
            }
            .description {
                color: #434959;
                width: 50%;
                h4 {
                    font-size: 40px;
                }
                p {
                    color: #9b9b9a;
                    text-align: left;
                }
                .buttons {
                    margin-top: 70px;
                    a {
                        text-decoration: none;
                        padding: 25px 40px;
                        border-radius: 100px;
                        font-size: 16px;
                    }
                }
            }
        }
    }
    .upper-wave {
        margin-bottom: -5px;
        margin-left: -6px;
    }
    .university-year {
        background-color: #e56768;
        display: flex;
        flex-direction: column;
        align-items: center;
        .top-img {
            margin-top: 100px;
            height: 75px;
        }
        h3 {
            margin-top: 30px;
            margin-bottom: 35px;
            color: white;
            font-size: 50px;
            background-color: #db2a2c;
        }
        .timeline {
            height: 500px;
            display: flex;
            align-items: center;
            position: relative;
            .times-dots {
                display: flex;
                flex-direction: column;
                width: 350px;
                position: absolute;
                bottom: 0;
                left: 0;
                text-align: center;
                .times-dot-title {
                    font-weight: 700;
                    font-size: 18px;
                    color: white;
                    margin-bottom: 15px;
                }
                .time-dot-description {
                    font-family: sans-serif;
                    color: white;
                    line-height: 23px;
                    font-size: 15px;
                }
                &:nth-of-type(1) {
                    left: 40px;
                    top: 350px;
                }
                &:nth-of-type(2) {
                    left: 268px;
                    top: 60px;
                }
                &:nth-of-type(3) {
                    left: 497px;
                    top: 350px;
                }
                &:nth-of-type(4) {
                    left: 726px;
                    top: 60px;
                }
            }
        }
    }

</style>