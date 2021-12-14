<template>
    <div class="container">
        <div class="background-image1">
            <Section
                titleImage="Books-icon.png"
                title="Thousands of courses for any type of student"
                Paragraph="At EduPrime, it doesn't matter what domain you wishto pursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides."
                Button="Browse through courses"
                ButtonType="button-3"
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
                <li 
                    class="facultie" 
                    :class="ActiveFacultie == i ? 'active' : ''" 
                    v-for="(facultie, i) in Faculties" 
                    :key="`facultie-${i}`" 
                    @click="activate(i)"
                >
                    <img :src="require(`../assets/${facultie.IconImg}`)" alt="">
                    <h4>{{facultie.Name}}</h4>
                </li>
            </ul>
            <div 
                class="active-facultie"
                v-for="(facultie, i) in Faculties" 
                :key="`facultie-${i}`"
                v-show="ActiveFacultie == i"
            >
                <img :src="require(`../assets/${facultie.Image}`)" alt="">
                <div class="description">
                    <h4>
                        {{facultie.Name}}
                    </h4>
                    <p>
                        {{facultie.Description}}
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
        <Section
            class="section-2"
            titleImage="Exam-icon.png"
            title="The most efficient examination method"
            Paragraph="EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject."
            ParagraphDim="medium"
            Button="Discover the Method"
            ButtonType="button-4"
            image="Exam-Illustration.png"
        />
        <Section
            class="section-3"
            Direction="row-reverse"
            titleImage="Exam-icon-1.png"
            title="Variable fees for international students"
            Paragraph="EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject."
            ParagraphDim="medium"
            Button="List of Fees"
            ButtonType="button-4"
            image="Girl-Illustration.png"
        />
        <div class="newsletter">
            <div class="container-newsletter">
                <h3>
                    Subscribe Now to Our Newsletter !
                </h3>
                <div class="form">
                    <input type="email" placeholder="Email address...">
                    <button><i class="fas fa-paper-plane"></i></button>
                </div>
            </div>
        </div>
        <div class="partners">
            <h3>
                Partners
            </h3>
            <p>
                Leverage agile frameworks to provide a robust synopsis for high level<br>
                overviews. Iterative approaches to corporate strategy.
            </p>
            <ul>
                <li v-for="(partner, i) in Partners" :key="`${i}`">
                    <img :src="require(`@/assets/${Partners[i]}`)" alt="">
                </li>
            </ul>
            <img class="lower-image" src="../assets/background-wave3.png" alt="">
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
                    IconImg: 'Gavel-v2.png',
                    Name: 'Law Faculty',
                    Image: 'Gavel-Illustration-e1556884768193.png',
                    Description: 'Learning from world-leading academics and practitioners, you’ll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions.'
                },
                {
                    IconImg: 'Coins-tabs-v2.png',
                    Name: 'Economy',
                    Image: 'Economy.png',
                    Description: 'Economics focuses on the behaviour and interactions of economic agents and how economies work. Microeconomics analyzes basic elements in the economy, including individual agents and markets, their interactions, and the outcomes of interactions, including unemployment of resource.'
                },
                {
                    IconImg: 'Medicine-tabs-v2.png',
                    Name: 'Medicine',
                    Image: 'Medicine.png',
                    Description: 'Medicine is the science and practice of establishing the diagnosis, prognosis, treatment, and prevention of disease. Medicine encompasses a variety of health care practices evolved to maintain and restore health by the prevention and treatment of illness.'
                },
                {
                    IconImg: 'Computer-tabs-v2.png',
                    Name: 'Computer Science',
                    Image: 'Computer-Science.png',
                    Description: 'Computer science is the study of processes that interact with data and that can be represented as data in the form of programs. It enables the use of algorithms to manipulate, store, and communicate digital information. A computer scientist studies the theory of computation software systems.'
                },
                {
                    IconImg: 'Palette-tabs-v2.png',
                    Name: 'Graphic Design',
                    Image: 'Graphic-Design.png',
                    Description: 'Graphic design is the process of visual communication and problem-solving through the use of typography, photography and illustration. The field is considered a subset of visual communication and communication design, but sometimes the term ``graphic design`` is used synonymously.'
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
            ],

            Partners: [
                'partner-2.png',
                'partner-3.png',
                'partner-4.png',
                'partner-5.png',
                'partner-6.png',
                'partner-8.png',
                'partner-1.png',
                'partner-7.png',

            ],

            ActiveFacultie: 0,
        }
    },

    components: {
        Section,
        Card1,
        Card2,
    },

    methods: {
        activate (i) {
            this.ActiveFacultie = i
        }
    },

}
</script>

<style lang="scss" scoped>
    @import '@/styles/Global.scss';
    .container {
        overflow-x: hidden;
    }
    .background-image1 {
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
                color: $primary_color;
                transition: 0.5s;
                img {
                    height: 100%;
                    margin-bottom: 20px;
                }
                &.active {
                    background-color: $primary_color;
                    img {
                        filter: brightness(3);
                    }
                    h4 {
                        color: white;
                    }
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
        background-color: $primary_color;
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
    .section-2 {
        height: 550px;
    }
    .section-3 {
        height: 550px;
        margin-bottom: 100px;
    }
    .newsletter {
        display: flex;
        justify-content: center;
        background-color: $primary_color;
        .container-newsletter {
            height: 200px;
            width: 70%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            h3 {
                font-size: 35px;
                color: white;
            }
            .form {
                position: relative;
                input {
                    height: 65px;
                    width: 400px;
                    padding: 30px;
                    font-family: sans-serif;
                    font-size: 15px;
                    font-weight: 500;
                    border-radius: 100px;
                    border: none;
                }
                button {
                    position: absolute;
                    height: 67px;
                    width: 67px;
                    background-color: #e5d45d;
                    border-radius: 50%;
                    border: none;
                    color: white;
                    font-size: 20px;
                    right: -1px;
                    bottom: -1px;
                    cursor: pointer;
                    transition: 0.5s;
                    &:hover {
                        background-color: #dd3333;
                    }
                }
            }
        }
    }
    .partners {
        height: 600px;
        overflow: hidden;
        .lower-image {
            background-color: #f7f8fa;
            width: 150%;
        }
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        padding: 50px;
        h3 {
            color: #3d404f;
            font-size: 50px;
            margin-bottom: 40px;
        }
        p {
            font-family: sans-serif;
            margin-bottom: 20px;
        }
        ul {
            list-style: none;
            display: flex;
            height: 50px;
            li {
                height: 100%;
                img {
                    height: 100%;
                    margin: 20px;
                    filter: opacity(0.3);
                    transition: 0.5s;
                    background-color: none;
                    &:hover {
                        filter: opacity(1);
                    }
                }
            }
        }
    }

</style>