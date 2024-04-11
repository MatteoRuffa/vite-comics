<template>
    <main>
        <div class="jumbotron"></div>
        <div class="container">
            <h3 class="title">current series</h3>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    main {
        background-color: $dark;
        .jumbotron {
            background-image: url('/img/jumbotron.jpg');
            height: 300px;
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