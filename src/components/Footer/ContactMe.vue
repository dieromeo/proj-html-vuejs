<script>
import FooterBar from './FooterBar.vue';

export default {
    name: 'ContactMe',
    data() {
        return {
            title: 'Contact me',
            info: { location: '457 BigBlue Street, NY 10013', phone: '(315) 5512-2579', email: 'everlead@mikado.com' }
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
            <li>
                <font-awesome-icon icon="fa-solid fa-location-dot" />
                <span>{{ info.location }}</span>
            </li>
            <li>
                <font-awesome-icon icon="fa-solid fa-phone" />
                <span>{{ info.phone }}</span>
            </li>
            <li>
                <font-awesome-icon icon="fa-solid fa-envelope" />
                <span>{{ info.email }}</span>
            </li>
        </ul>
        <div class="input-text">
            <h3>Subscribe</h3>
            <input type="text" placeholder="Your Name">
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.input-text {
    position: relative;

    h3 {
        position: absolute;
        bottom: 5px;
        right: 0;
        color: $white;
        z-index: 10;
    }
}

input {
    outline: none;
    border-width: 0 0 2px;
    width: 100%;
    background-color: transparent;
    margin-top: 40px;
    color: $white;
    padding: 5px 0;
}

svg {
    margin-right: 10px;
}
</style>