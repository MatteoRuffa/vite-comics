<template>
    <header class="container">
        <div><img src="/img/dc-logo.png" alt=""></div>
        <div>
            <ul>
                <li v-for="item in navbar" :key="item.name">
                    <a :href="item.link">{{ item.name }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data () {
            return {
                navbar: [
                    {name: 'Characters', link: '#'},
                    {name: 'Comics', link: '#'},
                    {name: 'Movies', link: '#'},
                    {name: 'TV', link: '#'},
                    {name: 'Games', link: '#'},
                    {name: 'Collectibles', link: '#'},
                    {name: 'Videos', link: '#'},
                    {name: 'Fans', link: '#'},
                    {name: 'News', link: '#'},
                    {name: 'Shop', link: '#'}
                ]   
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;

        ul {
            display: flex;
            gap: 20px;
            list-style: none;

            a {
                text-decoration: none;
                color: $dark;
                text-transform: uppercase;
                font-weight: 500;
                padding-bottom: 50px;
            }

            a:hover {
                color: $text-hover;
                border-bottom: 6px solid $text-hover;
            }
        }
    }
</style>