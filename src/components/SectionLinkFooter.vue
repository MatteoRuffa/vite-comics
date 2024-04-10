<template>
    <section>
        <div class="container">
            <div>
                <div><h5>dc comics</h5></div>
                <div><h5>shop</h5></div>
            </div>
            <div><h5>dc</h5></div>
            <div><h5>sites</h5></div>
        </div>

    </section>
</template>

<script>
    export default {
        name: 'SectionLinkFooter',
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    section {
        background-image: url('/img/footer-bg.jpg');
        padding: 40px 0;
        h5 {
            text-transform: uppercase;
            color: $light;
        }

        .container {
            display: flex;
            justify-content: start;
            align-items: flex-start;
            gap: 20px;
        }
    }

</style>