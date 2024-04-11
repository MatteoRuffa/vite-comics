<template>
    <section>
        <div class="container">
            <div>
                <div>
                    <h5>dc comics</h5>
                    <ul>
                        <li v-for="item in links.dccomics" :key="item.name">
                            <a :href="item.link">{{ item.name }}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h5>shop</h5>
                    <ul>
                        <li v-for="item in links.shop" :key="item.name">
                            <a :href="item.link">{{ item.name }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div>
                <h5>dc</h5>
                <ul>
                    <li v-for="item in links.dc" :key="item.name">
                        <a :href="item.link">{{ item.name }}</a>
                    </li>
                </ul>
            </div>
            <div>
                <h5>sites</h5>
                <ul>
                    <li v-for="item in links.sites" :key="item.name">
                        <a :href="item.link">{{ item.name }}</a>
                    </li>
                </ul>
            </div>
        </div>

    </section>
</template>

<script>
import { links } from '../data/store';
    export default {
        name: 'SectionLinkFooter',
        data () {
            return {
                links: links,
            }
        }
    }
    
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
    section {
        background-image: url('/img/dc-logo-bg.png'), url('/img/footer-bg.jpg');
        background-repeat: no-repeat, no-repeat;
        background-size: 600px, cover;
        background-position: calc(100% - 250px), center;
        padding: 60px 0;
        

        .container {
            display: flex;
            justify-content: start;
            align-items: flex-start;
            gap: 20px;
            h5 {
            text-transform: uppercase;
            color: $light;
            padding: 10px 0;
            }
            ul {
                list-style: none;
                padding: 0;
                
                a{
                    text-decoration: none;
                    color: $text-gray;
                    font-size: 0.9rem;
                }
                a:hover {
                    color: $light;
                }
            }
        }
    }

</style>