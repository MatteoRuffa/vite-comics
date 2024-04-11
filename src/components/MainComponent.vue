<template>
    <main>
        <div class="jumbotron"></div>
        <div class="container">
            <h3 class="title">current series</h3>
            <CardsComponent :items="comics"/>
        </div>
    </main>
</template>

<script>
import { comicsData } from '../data/store';
import CardsComponent from './CardsComponent.vue';
    export default {
        name: 'MainComponent',
        components: {
            CardsComponent,
        },
        data() {
            const comics = comicsData.map((item) => {
                return {
                    thumb: item.thumb,
                    price: item.price,
                    series: item.series,
                    type: item.type,
                    showPrice: false
                }
            })
            return {
                comics
            }
        },
        
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    main {
        background-color: $dark;
        .jumbotron {
            background-image: url('/img/jumbotron.jpg');
            height: 400px;
            background-size: cover;
        }
        h3 {
            background-color: $text-hover;
            color: $light;
            display: inline-block;
            padding: 10px 20px;
            text-transform: uppercase;
            transform: translateY(-50%);
        }
    }
</style>