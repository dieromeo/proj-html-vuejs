<script>
import SmallRightArrow from '../SmallRightArrow.vue';
import SmallLeftArrow from '../SmallLeftArrow.vue'
import TeamCard from './TeamCard.vue';

export default {
    name: 'Team',
    components: { SmallRightArrow, SmallLeftArrow, TeamCard },
    data() {
        return {
            image: { url: '../../../public/img/h1-img-01.jpg', alt: 'Jason Bickford' },
            cards: [
                { title: 'Jason Bickford', subtitle: 'Fouder and Executive Director', paragraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ...' }
            ]
        }

    }
}
</script>

<template>
    <section>
        <div class="team big-container">
            <div class="small-container">
                <div class="image-container">
                    <img :src="image.url" :alt="image.alt">
                    <div class="arrows">
                        <SmallLeftArrow />
                        <SmallRightArrow />
                    </div>
                </div>
                <div class="cards-container" v-for="card in cards">
                    <TeamCard :titolo="card.title" :sottotitolo="card.subtitle" :paragrafo="card.paragraph" />
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    background-color: $team-bg;
}

.team {
    background-image: url('../../../public/img/svg-4.svg');
    background-repeat: no-repeat;
    background-position-x: 98%;
    background-position-y: 15%;

    .small-container {
        padding: 140px 0;
        position: relative;
    }

    .image-container {
        width: 700px;
        position: relative;

        img {
            width: 100%;
            display: block;
        }
    }

    .cards-container {
        position: absolute;
        right: 0;
        top: 25%;
    }
}

.arrows {
    display: flex;
    gap: 10px;
    position: absolute;
    left: 0;
    bottom: 0;
    background-color: $secondary-color;
    color: $white;
    padding: 22px 25px;
}
</style>