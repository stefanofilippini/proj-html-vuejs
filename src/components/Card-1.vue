<template>
    <div class="card">
        <h1>{{ Title }}</h1>
        <div class="date">
            <span><i class="far fa-calendar-alt"></i> {{ Dates }}</span>
        </div>
        <p>
            {{ Paragraph }}
        </p>
        <div class="buttons">
            <a href="#" class="button-4"><i class="fas fa-plus"></i> {{ Button }}</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card1',

    props: {
        Title: String,
        Dates: String,
        Paragraph: String,
        Button: String,
    },
}
</script>

<style lang="scss" scoped>
    .card {
        margin-bottom: 100px;
        position: relative;
        width: 370px;
        text-align: center;
        background-color: white;
        padding: 30px 30px 45px;
        border-radius: 20px;
        box-shadow: rgba(0, 0, 0, 0.1) -4px 9px 25px -6px;
        h1 {
            font-size: 30px;
            color: #3d404f;
            margin-bottom: 5px;
        }
        .date {
            margin-bottom: 10px;
            span {
                font-size: 13px;
                font-family: sans-serif;
                color: #82848e;
                .far {
                    font-size: 15px;
                }
            }
        }
        p {
            font-family: sans-serif;
            color: #82848e;
            overflow: hidden;
            line-height: 27px;
            display: -webkit-box;
            -webkit-box-orient: vertical;
            -webkit-line-clamp: 2;
        }
        .buttons {
            margin-top: 70px;
            position: absolute;
            transform: translate(-50%, -50%);
            bottom: -20px;
            left: 50%;
            .fas {
                margin-right: 5px;
            }
            a {
                text-decoration: none;
                padding: 10px 20px;
                border-radius: 100px;
                font-size: 14px;
                box-shadow: rgba(0, 0, 0, 0.1) -4px 9px 25px -6px;
            }
        }
    }
</style>