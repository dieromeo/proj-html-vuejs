<script>
import MainButton from '../MainButton.vue';
export default {
    name: 'HeaderPreview',
    props: ['titolo', 'contenuto'],
    components: { MainButton },
    data() {
        return {
            firstButton: 'Read more',
            secondButton: 'purchase'
        }
    }

}
</script>

<template>
    <div class="info">
        <h1>{{ titolo }}<span class="dot">.</span></h1>
        <p>{{ contenuto }}</p>
        <div class="buttons">
            <MainButton :testoBottone="firstButton" />
            <MainButton class="purchase" :testoBottone="secondButton" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables.scss' as *;

.info {
    margin-top: 300px;
    margin-left: 220px;
    max-width: 600px;

    h1 {
        font-size: 70px;
    }

    p {
        font-size: 20px;
        margin-top: 30px;
        color: $text-secondary;
    }

    .buttons {
        display: flex;
        gap: 20px;
        margin-top: 50px;

        .purchase {
            color: $white;
            background-color: $secondary-color;
        }
    }
}
</style>