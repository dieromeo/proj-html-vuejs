<script>
import FooterBar from './FooterBar.vue';

export default {
    name: 'ImportantLinks',
    data() {
        return {
            title: 'Important Links',
            links: [
                { text: 'About me', href: '#' },
                { text: 'About us', href: '#' },
                { text: 'Language packs', href: '#' },
                { text: 'Become a coach', href: '#' },
                { text: 'Monthly events', href: '#' },
            ]
        };
    },
    components: { FooterBar }
}
</script>

<template>
    <div>
        <h2>{{ title }}</h2>
        <FooterBar />
        <ul>
            <li v-for="link in links">
                <a :href="link.href">{{ link.text }}</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped></style>