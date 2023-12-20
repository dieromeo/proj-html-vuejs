<script>
export default {
    name: 'Carousel',
    data() {
        return {
            images: [
                { url: '../../../public/img/h1-img-04.jpg', alt: 'Fisrt image' },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="img-container" v-for="image in images">
            <img :src="image.url" :alt="image.url">
            <div class="play">
                <font-awesome-icon icon="fa-solid fa-play" />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.img-container {
    position: relative;

    .play {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 45px;
        color: $white;
        cursor: pointer;
    }
}
</style>