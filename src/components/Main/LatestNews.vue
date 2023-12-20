<script>
import BigLeftArrow from '../BigLeftArrow.vue';
import BigRightArrow from '../BigRightArrow.vue';
import Bar from '../Bar.vue';
import LatestNewsCard from './LatestNewsCard.vue';

export default {
    name: 'LatestNews',
    components: { BigLeftArrow, BigRightArrow, Bar, LatestNewsCard },
    data() {
        return {
            title: 'Latest news',
            subtitle: 'Lorem ipsum sit dolor amet, consectetur adipiscing elit',
            cards: [
                {
                    img: { url: '../../../public/img/h1-blog-img-02.jpg', alt: 'Next investment' },
                    data: 'May 5, 2019',
                    author: 'Amanda Doe',
                    title: 'Next Investment',
                    paragraph: 'Lorem ispum sit dolor amet, consectetur adipiscing elit, sed eius mas tellus dolor...'
                },
                {
                    img: { url: '../../../public/img/h1-blog-img-03.jpg', alt: 'Team building' },
                    data: 'May 5, 2019',
                    author: 'Amanda Doe',
                    title: 'Team Buildig',
                    paragraph: 'Lorem ispum sit dolor amet, consectetur adipiscing elit, sed eius mas tellus dolor...'
                },
                {
                    img: { url: '../../../public/img/h1-blog-img-04.jpg', alt: 'Business day' },
                    data: 'May 5, 2019',
                    author: 'Amanda Doe',
                    title: 'Business Day',
                    paragraph: 'Lorem ispum sit dolor amet, consectetur adipiscing elit, sed eius mas tellus dolor...'
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="big-container">
            <div class="bg-image">
                <img src="../../../public/img/svg-4.svg" alt="">
            </div>
            <BigLeftArrow class="absolute-left" />
            <BigRightArrow class="absolute-right" />
            <div class="small-container">
                <div class="info-section">
                    <h2>{{ title }}<span class="dot">.</span></h2>
                    <p>{{ subtitle }}</p>
                    <Bar />
                </div>
                <ul>
                    <li v-for="card in cards">
                        <LatestNewsCard :immagine="card.img" :data="card.data" :autore="card.author" :titolo="card.title"
                            :paragrafo="card.paragraph" />
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    background-color: $team-bg;

    .big-container {
        height: 950px;
        position: relative;
        padding: 120px 0 140px 0;

        .bg-image {
            position: absolute;
            left: 0;
            top: -95px;
        }
    }

    .small-container {
        text-align: center;

        .info-section {
            display: flex;
            flex-direction: column;
            align-items: center;

            h2 {
                font-size: 45px;
                margin-bottom: 20px;
            }

            p {
                color: $text-secondary;
                margin-bottom: 30px;
            }
        }

        ul {
            display: flex;
            gap: 35px;
            margin-top: 70px;
        }
    }
}
</style>