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
            <img class="top-img" src="../assets/upcoming-events-calendar-icon.png" alt="">
            <h3>Upcoming Events</h3>
            <div class="sessions">
                <Card1 v-for="(session, i) in Sessions" :key="`session-${i}`"
                    :Title= "session.Title"
                    :Dates="session.Date"
                    :Paragraph="session.Par"
                    :Button="session.Button"
                />
            </div>
            <div class="buttons">
                <a href="#" class="button-1">View All Events</a>
            </div>
        </section>
        <img class="lower-wave" src="../assets/svg/svg-1.svg" alt="">
        <div class="courses-container">
            <h3>Latest Courses</h3>
            <div class="courses">
                <Card2 v-for="(course , i) in Courses" :key="`course-${i}`"
                    :Image ="course.Img"
                    :Title ="course.Title"
                    :Teacher ="course.Teacher"
                    :Price ="course.Price"
                    :Button ="course.Button"
                />
            </div>
        </div>
    </div>
</template>

<script>
import Section from '@/components/Section.vue'
import Card1 from '@/components/Card-1.vue'
import Card2 from '@/components/Card-2.vue'

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
            ],

            Sessions: [
                {
                    Title: 'Coaching Sessions',
                    Date: '20 May 21:30 PM',
                    Par: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure, id! Quo suscipit veniam, ut illum nostrum accusamus voluptas quaerat accusantium laborum exercitationem itaque doloremque rem. Id porro sit quasi inventore.',
                    Button: 'Find More'
                },
                {
                    Title: 'Coaching Sessions',
                    Date: '24 Mar 18:00 PM',
                    Par: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure, id! Quo suscipit veniam, ut illum nostrum accusamus voluptas quaerat accusantium laborum exercitationem itaque doloremque rem. Id porro sit quasi inventore.',
                    Button: 'Find More'
                },
                {
                    Title: 'Coaching Sessions',
                    Date: '12 Feb 12:30 PM',
                    Par: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure, id! Quo suscipit veniam, ut illum nostrum accusamus voluptas quaerat accusantium laborum exercitationem itaque doloremque rem. Id porro sit quasi inventore.',
                    Button: 'Find More'
                },
            ],

            Courses: [
                {
                    Img: 'Decisions-icon.png',
                    Title: 'Make Better Decisions',
                    Teacher: 'James Collins',
                    Price: '$21.00',
                    Button: 'View Course'
                },
                {
                    Img: 'Speaker-icon.png',
                    Title: 'How to be a speaker',
                    Teacher: 'James Collins',
                    Price: 'Free',
                    Button: 'View Course'
                },
                {
                    Img: 'Network-icon.png',
                    Title: 'Network Introductions',
                    Teacher: 'James Collins',
                    Price: 'Free',
                    Button: 'View Course'
                },
                {
                    Img: 'Brand-icon.png',
                    Title: 'Brand Management',
                    Teacher: 'James Collins',
                    Price: 'Free',
                    Button: 'View Course'
                },
            ]
        }
    },

    components: {
        Section,
        Card1,
        Card2,
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
            &:last-of-type {
                margin-top: 50px;
            }
        }
        h3 {
            margin-top: 30px;
            margin-bottom: 35px;
            color: white;
            font-size: 50px;
            background-color: #db2a2c;
            &:last-of-type {
                background-color: transparent;
            }
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
        .sessions {
            width: 65%;
            display: flex;
            justify-content: space-between;
        }
        .buttons {
            margin: 100px 0px;
            a {
                text-decoration: none;
                padding: 25px 40px;
                border-radius: 100px;
                font-size: 16px;
            }
        }
    }
    .lower-wave {
        margin-top: -1px;
        margin-left: -7px;
    }
    .courses-container {
        display: flex;
        flex-direction: column;
        width: 70%;
        margin: 0 auto;
        margin-bottom: 100px;
        h3 {
            color: #3d404f;
            font-size: 40px;
            margin-bottom: 60px;
        }
        .courses {
            display: flex;
            justify-content: space-between;
        }
    }

</style>