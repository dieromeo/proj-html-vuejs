<script>
import About from './About.vue';
import ContactMe from './ContactMe.vue';
import FooterBottom from './FooterBottom.vue';
import ImportatLinks from './ImportatLinks.vue';
import Footertwitter from './footertwitter.vue';

export default {
    name: 'FooterComponent',
    components: { About, Footertwitter, ImportatLinks, ContactMe, FooterBottom }
}
</script>

<template>
    <footer>
        <div class="top">
            <div class="small-container">
                <About class="about" />
                <Footertwitter />
                <ImportatLinks />
                <ContactMe />
            </div>
        </div>
        <FooterBottom />
    </footer>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.top {
    background-color: $footer-bg;
}

.small-container {
    display: flex;
    justify-content: space-between;
    padding: 110px 0;

    div {
        max-width: 305px;

        :deep(h2) {
            color: $white;
        }

        :deep() {
            color: $text-secondary;
            font-size: 16px;
            line-height: 25px;
        }

        :deep(svg) {
            color: $secondary-color;
        }

        :deep(a) {
            color: $text-secondary;
        }
    }

    .about {
        :deep(svg) {
            color: $text-main;
        }
    }
}
</style>