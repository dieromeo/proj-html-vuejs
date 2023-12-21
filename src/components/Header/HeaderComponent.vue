<script>
import BigLeftArrow from '../BigLeftArrow.vue';
import BigRightArrow from '../BigRightArrow.vue';
import HeaderPreview from './HeaderPreview.vue';
import Topbar from './Topbar.vue';

export default {
    name: 'HeaderComponent',
    components: { Topbar, BigLeftArrow, BigRightArrow, HeaderPreview },
    data() {
        return {
            status: 'first',
            content: [
                { title: 'Our Team', paragraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit sed eiusmod tempor incididunt ut labore et dolore magna aliqua.' }
            ]
        }
    },
    methods: {
        // scorrere carosello in avanti
        nextStatus() {
            this.status = 'second';
        },
        // scorrere carosello indietro
        prevStatus() {
            this.status = 'first';
        },
    }
}
</script>

<template>
    <header :class="status">
        <div class="big-container">
            <Topbar />
            <BigLeftArrow class="absolute-left" @click="prevStatus" />
            <BigRightArrow class="absolute-right" @click="nextStatus" />
            <HeaderPreview :titolo="content[0].title" :contenuto="content[0].paragraph" />
        </div>
    </header>
</template>

<style lang="scss" scoped>
header.first {
    background-image: url('../../../public/img/rev-slider-main-home-img-03.jpg');
}

header.second {
    background-image: url('../../../public/img/rev-slider-main-home-img-02.png');
}

header {
    height: 890px;

    .big-container {
        position: relative;
        height: 100%;
    }
}
</style>