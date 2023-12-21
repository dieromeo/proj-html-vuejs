<script>
import Bar from '../Bar.vue';
import SpecialtiesCard from './SpecialtiesCard.vue';

export default {
    name: 'Specialties',
    data() {
        return {
            title: 'Our specialties',
            content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
            cards: [
                { url: '../../public/img/svg-0.svg', title: 'Knowing', content: 'Lorem ipsum dolor sit amet, quis consect' },
                { url: '../../public/img/svg-1.svg', title: 'Selling', content: 'Lorem ipsum dolor sit amet, quis consect' },
                { url: '../../public/img/svg-2.svg', title: 'Learning', content: 'Lorem ipsum dolor sit amet, quis consect' },
                { url: '../../public/img/svg-3.svg', title: 'Contact', content: 'Lorem ipsum dolor sit amet, quis consect' },
            ]
        };
    },
    components: { Bar, SpecialtiesCard }
}
</script>

<template>
    <section class="">
        <div class="specialties-content big-container">
            <!-- titolo e contenuto  -->
            <h2>{{ title }}<span class="dot">.</span></h2>
            <p>{{ content }}</p>
            <Bar />
            <!-- cards  -->
            <ul>
                <li v-for="card in cards">
                    <SpecialtiesCard :immagine="card.url" :titolo="card.title" :contenuto="card.content" />
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    text-align: center;
    position: relative;
    height: 640px;
    background-color: $team-bg;

    .specialties-content {
        display: flex;
        padding: 130px;
        flex-direction: column;
        align-items: center;
        position: absolute;
        z-index: 10;
        background-color: $white;
        top: -75px;
        left: 0;
        right: 0;

        h2 {
            font-size: 50px;
        }

        p {
            color: $text-secondary;
            margin: 15px 0 30px 0;
            font-size: 20px;
        }

        ul {
            margin-top: 70px;
            display: flex;
            gap: 120px;
        }
    }
}
</style>