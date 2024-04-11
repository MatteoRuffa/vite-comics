<template>
    <div class="row">
        <div class="col-12 col-md-4 col-lg-2" v-for="(item, index) in items" :key="index">
            <div class="image" @mouseover="item.showPrice = true" @mouseout="item.showPrice = false">
                <img :src="item.thumb" :alt="item.series">
                <span class="price" v-if="item.showPrice">{{ item.price }}</span>
            </div>
            <h5>{{ item.series }}</h5>
        </div>
        <div class="text-center"><a href="#">load more</a></div>
    </div>
</template>

<script>
    export default {
        name: 'CardsComponent',
        props: ['items'],
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;

    .row {
        .image {
            position: relative;
            padding: 20px 0;
            img {
                width: 100%;
                // height: 300px;
                transition: opacity 0.3s ease;
                &:hover {
                    opacity: 0.3;
                    
                    cursor: pointer;
                }
            }
            .price {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                color: $light;
                font-weight: 700;
                font-size: 2rem;
            }
        }
        h5 {
            color: $light;
            text-transform: uppercase;
            padding: 10px 0;
        }
        .text-center {
            padding: 30px;
        }
        a {
            text-decoration: none;
            color: $light;
            text-transform: uppercase;
            font-weight: 500;
            font-size: 1.2rem;
            padding: 10px 100px;
            background-color: $text-hover;
        }
    }

    @media screen and (max-width: 1200px) {
        .image {
        img {
            height: auto;
        }
    }
    }
    
</style>