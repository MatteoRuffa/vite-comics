<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="item in navbarFooter" :key="item.name">
                    <a :href="item.link">
                        <img :src="item.img" :alt="item.name">
                        <span>{{ item.name }}</span>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'NavbarFooter',
        data () {
            return{
                navbarFooter: [
                    {name: 'digital comics', link: '#', img: '/img/buy-comics-digital-comics.png'},
                    {name: 'dc merchandise', link: '#', img: '/img/buy-comics-merchandise.png'},
                    {name: 'subscription', link: '#', img: '/img/buy-comics-subscriptions.png'},
                    {name: 'comic shop locator', link: '#', img: '/img/buy-comics-shop-locator.png'},
                    {name: 'dc power visa', link: '#', img: '/img/buy-dc-power-visa.svg'}
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    section {
        background-color: $text-hover;
    }
</style>