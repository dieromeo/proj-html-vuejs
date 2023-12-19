<script>
export default {
    name: 'Navbar',
    data() {
        return {
            list: [
                { title: 'Homes', link: '#' },
                { title: 'Pages', link: '#' },
                { title: 'Blog', link: '#' },
                { title: 'Shop', link: '#' },
                { title: 'Events', link: '#' },
                { title: 'Elements', link: '#' },
            ]
        }
    }
}
</script>

<template>
    <nav>
        freccia
        <ul>
            <li v-for="element in list">
                <a :href="element.link">{{ element.title.toUpperCase() }}</a>
            </li>
        </ul>
        icone
    </nav>
</template>

<style lang="scss" scoped>
nav {
    display: flex;

    ul {
        display: flex;
        gap: 45px;
    }
}
</style>