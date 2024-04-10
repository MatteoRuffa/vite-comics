<template>
    <main>
        <div class="container">
            <h2>--> Contents goes here <--</h2> 
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
        h2 {
            color: $light;
            padding: 20px;
            margin: 0;
        }
    }
</style>