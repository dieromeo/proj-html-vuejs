<script>
import ReadMore from '../ReadMore.vue';

export default {
    name: 'LatestNewsCard',
    props: ['immagine', 'data', 'autore', 'titolo', 'paragrafo'],
    components: { ReadMore }
}
</script>

<template>
    <div class="cards">
        <!-- immagine  -->
        <div class="img-container">
            <img :src="immagine.url" :alt="immagine.alt">
            <!-- didascalia immagine  -->
            <div class="business">
                <font-awesome-icon icon="fa-solid fa-tag" />
                <p>Business, Leading</p>
            </div>
        </div>
        <div class="card-content">
            <!-- info carta e contenuto  -->
            <div class="card-info">
                <font-awesome-icon icon="fa-regular fa-clock" />
                <p>{{ data }}</p>
                <font-awesome-icon icon="fa-regular fa-user" />
                <p>{{ autore }}</p>
            </div>
            <h2>{{ titolo }}</h2>
            <p class="paragraph">{{ paragrafo }}</p>
            <ReadMore />
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

.card-content {
    .card-info {
        font-size: 12px;
        margin-top: 40px;
        display: flex;

        svg {
            color: $secondary-color;
        }

        p {
            margin: 0 10px;
            color: $text-secondary;
        }
    }

    h2 {
        margin: 15px 0;
        font-size: 24px;
    }

    .paragraph {
        font-size: 14px;
        color: $text-secondary;
    }
}
</style>