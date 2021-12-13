<template>
    <div class="card">
        <img :src="require(`@/assets/${Image}`)" alt="">
        <h1>{{ Title }}</h1>
        <div class="card-attribute Teacher">
            <span><i class="far fa-user"></i>Teacher:</span><span>{{ Teacher }}</span>
        </div>
        <div class="card-attribute Price">
            <span><i class="far fa-money-bill-alt"></i>Price:</span><span>{{ Price }}</span>
        </div>
        <div class="buttons">
            <a href="#" class="button-4"><i class="far fa-eye"></i> {{ Button }}</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card2',

    props: {
        Image: String,
        Title: String,
        Teacher: String,
        Price: String,
        Button: String,
    },
}
</script>

<style lang="scss" scoped>
    .card {
        position: relative;
        text-align: center;
        background-color: white;
        padding: 30px 30px 30px;
        border-radius: 10px;
        box-shadow: rgba(0, 0, 0, 0.15) 0px 2px 8px;
        img {
            max-height: 80px;
            margin-bottom: 20px;
        }
        h1 {
            font-size: 19px;
            color: #223441;
            margin-bottom: 5px;
        }
        .card-attribute {
            margin-bottom: 10px;
            span {
                font-size: 13px;
                font-family: sans-serif;
                color: #82848e;
                margin-right: 5px;
                .far {
                    font-size: 14px;
                    margin-right: 5px;
                }
                &:last-of-type {
                    color: #6b6c74;
                    font-weight: 700;
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
            width: 100%;
            position: absolute;
            transform: translate(-50%, -50%);
            bottom: -20px;
            left: 50%;
            .far {
                margin-right: 5px;
            }
            a {
                text-decoration: none;
                padding: 10px 20px;
                border-radius: 100px;
                font-size: 14px;
                box-shadow: rgba(0, 0, 0, 0.15) 0px 2px 8px;
            }
        }
    }
</style>