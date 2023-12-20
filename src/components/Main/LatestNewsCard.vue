<script>
export default {
    name: 'LatestNewsCard',
    props: ['immagine', 'data', 'autore', 'titolo', 'paragrafo'],
}
</script>

<template>
    <div class="cards">
        <div class="img-container">
            <img :src="immagine.url" :alt="immagine.alt">
            <div class="business">
                <font-awesome-icon icon="fa-solid fa-tag" />
                <p>Business, Leading</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.img-container {
    max-width: 420px;
    position: relative;
    z-index: 10;

    img {
        width: 100%;
        display: block;
    }

    .business {
        display: flex;
        padding: 10px 20px;
        color: $white;
        background-color: $secondary-color;
        max-width: 165px;
        font-size: 13px;
        position: absolute;
        right: 15px;
        bottom: -10px;

        p {
            margin-left: 5px;
        }
    }
}
</style>