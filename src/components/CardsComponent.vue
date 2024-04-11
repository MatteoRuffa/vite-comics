<template>
    <div class="row">
        <div class="col-12 col-md-4 col-lg-2" v-for="(item, index) in items" :key="index">
            <div class="image"><img :src="item.thumb" :alt="item.series"></div>
            <h5>{{ item.series }}</h5>
    </div>
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
    .image {
        img {
        width: 100%;
        }
    }
    
</style>