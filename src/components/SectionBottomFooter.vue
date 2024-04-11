<template>
    <section>
        <div class="container">
            <div>
                <a href="#">sign-up now!</a>
            </div>
            <div>
                <span>follow us</span>
                <img src="/img/footer-facebook.png" alt="">
                <img src="/img/footer-twitter.png" alt="">
                <img src="/img/footer-youtube.png" alt="">
                <img src="/img/footer-pinterest.png" alt="">
                <img src="/img/footer-periscope.png" alt="">
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'SectionBottomFooter',
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    section {
        background-color: $bg-bottom-footer;
        padding: 30px 0;
        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;

            a {
            text-decoration: none;
            text-transform: uppercase;
            color: $light;
            border: 2px solid $text-hover;
            padding: 10px 20px;
            }

            span {
                color: $text-hover;
                text-transform: uppercase;
                font-weight: 700;
                padding: 0 20px;
            }
            img {
                padding: 0 10px;
                transition: transform 0.3s ease;
            }
            img:hover {
                transform: scale(1.5);
            }
        }
        
    }

</style>