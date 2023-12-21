<script>
import SmallRightArrow from '../SmallRightArrow.vue';
import SmallLeftArrow from '../SmallLeftArrow.vue'
import TeamCard from './TeamCard.vue';

export default {
    name: 'Team',
    components: { SmallRightArrow, SmallLeftArrow, TeamCard },
    data() {
        return {
            images: [
                { url: '../../../public/img/h1-img-01.jpg', alt: 'Jason Bickford', active: true },
                { url: '../../../public/img/h1-img-02.jpg', alt: 'Jason Bickford', active: false },
                { url: '../../../public/img/h1-img-03.jpg', alt: 'Jason Bickford', active: false },
            ],
            cards: [
                { title: 'Jason Bickford', subtitle: 'Fouder and Executive Director', paragraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ...', active: true },
                { title: 'Lorem Ipsum', subtitle: 'Fouder and Executive Director', paragraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ...', active: false },
                { title: 'Lorem Ipsum', subtitle: 'Fouder and Executive Director', paragraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ...', active: false },
            ],
            currentIndex: 0
        }

    },
    methods: {
        next() {
            if (this.currentIndex < this.images.length - 1 && this.currentIndex < this.cards.length - 1) {
                this.images[this.currentIndex].active = false;
                this.cards[this.currentIndex].active = false;
                this.currentIndex++;
                this.images[this.currentIndex].active = true;
                this.cards[this.currentIndex].active = true;
            }
        },
        prev() {
            if (this.currentIndex !== 0 && this.currentIndex !== 0) {
                this.images[this.currentIndex].active = false;
                this.cards[this.currentIndex].active = false;
                this.currentIndex--;
                this.images[this.currentIndex].active = true;
                this.cards[this.currentIndex].active = true;
            }
        }
    }
}
</script>

<template>
    <section>
        <div class="team big-container">
            <div class="small-container">
                <!-- immagine con frecce  -->
                <div class="image-container">
                    <img v-for="image in images" :src="image.url" :alt="image.alt" v-show="image.active === true">
                    <div class="arrows">
                        <SmallLeftArrow @click="prev" />
                        <SmallRightArrow @click="next" />
                    </div>
                </div>
                <!-- cards  -->
                <div class="cards-container" v-for="card in cards" v-show="card.active === true">
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