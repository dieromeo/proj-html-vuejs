<script>
import Socials from '../Socials.vue';
import FooterBar from './FooterBar.vue';

export default {
    name: 'About',
    data() {
        return {
            title: 'About',
            content: 'We created Everlead to effectively become the stepping stone towards meeting all your goals & achieving business success.'
        };
    },
    components: { Socials, FooterBar }
}
</script>

<template>
    <div>
        <h2>{{ title }}</h2>
        <FooterBar />
        <p>{{ content }}</p>
        <Socials class="footer-social" />
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.footer-social {
    :deep(div) {
        background-color: $white;
    }
}
</style>