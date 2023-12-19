<script>
import SmallRightArrow from '../SmallRightArrow.vue';

export default {
    name: 'Navbar',
    data() {
        return {
            list: [
                { title: 'Homes', link: '#', active: true },
                { title: 'Pages', link: '#', active: false },
                { title: 'Blog', link: '#', active: false },
                { title: 'Shop', link: '#', active: false },
                { title: 'Events', link: '#', active: false },
                { title: 'Elements', link: '#', active: false },
            ]
        };
    },
    components: { SmallRightArrow }
}
</script>

<template>
    <nav>
        <SmallRightArrow class="orange" />
        <ul>
            <li v-for="element in list">
                <a :href="element.link" :class="element.active === true ? 'orange' : ''">{{ element.title.toUpperCase()
                }}</a>
            </li>
        </ul>
        <font-awesome-icon icon="magnifying-glass" />
        <font-awesome-icon icon="bars" />
    </nav>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables.scss' as *;

.orange {
    color: $secondary-color;
}

nav {
    display: flex;
    align-items: center;

    ul {
        display: flex;
        gap: 45px;
        margin-left: 10px;
        font-size: 13px;
    }

    a {
        color: $text-main;
        font-weight: bold;
    }

    svg {
        margin-left: 40px;
        cursor: pointer;
    }
}
</style>