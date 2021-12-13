<template>
    <div class="container" :class="Direction">
        <div class="description">
            <img :src="require(`@/assets/${titleImage}`)" alt="">
            <h3>{{ title }}</h3>
            <p :class="ParagraphDim">{{Paragraph}}</p>
            <div class="buttons">
                <a :class="ButtonType" href="#">{{ Button }}</a>
            </div>
        </div>
        <div class="img">
            <img :src="require(`@/assets/${image}`)" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Section',

    props: {
        Direction: String,
        titleImage: String,
        title: String,
        Paragraph: String,
        ParagraphDim: String,
        Button: String,
        ButtonType: String,
        image: String,
    },

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
            &.row-reverse {
                flex-direction: row-reverse;
            }
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
                    &.medium {
                        width: 70%;
                    }
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