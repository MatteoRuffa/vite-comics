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
import { navbar } from '../data/store';
    export default {
        name: 'HeaderComponent',
        data () {
            return {
                navbar: navbar,
            }
        }
    };
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
                padding-bottom: 63px;
            }

            a:hover {
                color: $text-hover;
                border-bottom: 6px solid $text-hover;
            }
        }
    }
</style>