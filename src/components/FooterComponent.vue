<template>
    <footer>
        <NavbarFooter />
        <SectionLinkFooter />
        <SectionBottomFooter />
    </footer>
</template>

<script>
import NavbarFooter from './NavbarFooter.vue';
import SectionLinkFooter from './SectionLinkFooter.vue';
import SectionBottomFooter from './SectionBottomFooter.vue';
    export default {
        name: 'FooterComponent',
        components: {
            NavbarFooter,
            SectionLinkFooter,
            SectionBottomFooter
        }
    }
</script>

<style lang="scss" scoped>
    
</style>