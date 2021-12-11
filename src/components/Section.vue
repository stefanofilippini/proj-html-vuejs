<template>
  <div class="container">
            <div class="description">
                <img src="../assets/Books-icon.png" alt="">
                <h3>Thousands of courses for any type of student</h3>
                <p>At EduPrime, it doesn't matter what domain you wishto pursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides.</p>
                <div class="buttons">
                    <a class="button-3" href="#">Browse through courses</a>
                </div>
            </div>
            <div class="img">
                <img src="../assets/Graduation-Illustration.png" alt="">
            </div>
        </div>
</template>

<script>
export default {
    name: 'Section',

}
</script>

<style lang="scss" scoped>
    .container {
            width: 70%;
            height: 100%;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            .description {
                width: 50%;
                color: #3d404f;
                display: flex;
                flex-direction: column;
                img {
                    width: 10%;
                    margin-bottom: 20px;
                }
                h3 {
                    font-size: 50px;
                    margin-bottom: 40px;
                }
                p {
                    font-family: sans-serif;
                    line-height: 30px;
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
            .img {
                width: 40%;
                img {
                    width: 100%;
                }
            }
        }
</style>