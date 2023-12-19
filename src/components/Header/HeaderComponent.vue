<script>
import BigLeftArrow from '../BigLeftArrow.vue';
import BigRightArrow from '../BigRightArrow.vue';
import Topbar from './Topbar.vue';

export default {
    name: 'HeaderComponent',
    components: { Topbar, BigLeftArrow, BigRightArrow },
    data() {
        return {
            status: 'first'
        }
    },
    methods: {
        nextStatus() {
            this.status = 'second';
        },
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

.absolute-left {
    position: absolute;
    left: 0;
    top: 50%;
}

.absolute-right {
    position: absolute;
    right: 0;
    top: 50%;
}
</style>