<template>
    <footer>
        <NavbarFooter />
        <SectionLinkFooter />
    </footer>
</template>

<script>
import NavbarFooter from './NavbarFooter.vue';
import SectionLinkFooter from './SectionLinkFooter.vue';
    export default {
        name: 'FooterComponent',
        components: {
            NavbarFooter,
            SectionLinkFooter,
        }
    }
</script>

<style lang="scss" scoped>
    
</style>