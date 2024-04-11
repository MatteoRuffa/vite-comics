<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="item in navbarFooter" :key="item.name">
                    <a class="d-flex align-items-center " :href="item.link">
                        <img :src="item.img" :alt="item.name">
                        <div>{{ item.name }}</div>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
import { navbarFooter } from '../data/store';
    export default {
        name: 'NavbarFooter',
        data () {
            return{
                navbarFooter: navbarFooter,
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    section {
        background-color: $text-hover;
        padding:  20px 0;
        ul {
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 0;

            li {
                display: flex;
                align-items: center;
                padding: 10px;
                a {
                    text-decoration: none;
                    transition: transform 0.3s ease;
                    img {
                        width: 50px;
                        
                    }
                    
                    div {
                        text-transform: uppercase;
                        color: $light;
                        padding: 0 10px;
                        transition: transform 0.3s ease;
                    }
                }
                a:hover {
                    transform: scale(1.5);
                }
            }
        }
    }

@media screen and (max-width: 992px) {
    img {
        display: none;
    }
    
}
</style>