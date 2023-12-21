<script>
import BigLeftArrow from '../BigLeftArrow.vue';
import BigRightArrow from '../BigRightArrow.vue';

export default {
    name: 'testimonials',
    components: { BigLeftArrow, BigRightArrow },
    data() {
        return {
            testimonials: [
                { url: '../../../public/img/h3-img-04.png', alt: 'Cynthia Clark', name: 'Cynthia Clark', content: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit sed eiusmod tempor incididunt ut labore et dolore magna aliqua."', active: true, id: 1 },
                { url: '../../../public/img/h3-img-07.png', alt: 'Lorem ipsum', name: 'Lorem ipsum', content: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit sed eiusmod tempor incididunt ut labore et dolore magna aliqua."', active: false, id: 2 },
                { url: '../../../public/img/h3-img-08.png', alt: 'Lorem ispum', name: 'Lorem ipsum', content: '"Lorem ipsum dolor sit amet, consectetur adipiscing elit sed eiusmod tempor incididunt ut labore et dolore magna aliqua."', active: false, id: 3 },
            ],
            currentIndex: 0
        }
    },
    methods: {
        barWidth(index) {
            return (this.testimonials[index].id / this.testimonials.length) * 100;
        },
        next() {
            if (this.currentIndex < this.testimonials.length - 1) {
                this.testimonials[this.currentIndex].active = false;
                this.currentIndex++;
                this.testimonials[this.currentIndex].active = true;
            }
        },
        prev() {
            if (this.currentIndex !== 0) {
                this.testimonials[this.currentIndex].active = false;
                this.currentIndex--;
                this.testimonials[this.currentIndex].active = true;
            }
        }
    }
}
</script>

<template>
    <section>
        <div class="big-container">
            <!-- frecce  -->
            <BigLeftArrow class="absolute-left" @click="prev" />
            <BigRightArrow class="absolute-right" @click="next" />
            <!-- immagini  -->
            <div class="testimonial-content" v-for="(testimonial, index) in testimonials"
                v-show="testimonial.active === true">
                <img :src="testimonial.url" :alt="testimonial.alt">
                <!-- titolo e contenuto  -->
                <h2>{{ testimonial.name }}</h2>
                <p>{{ testimonial.content }}</p>
                <!-- barra del carosello  -->
                <div class="carousel-bar">
                    <span>0{{ testimonial.id }}</span>
                    <div class="bar">
                        <div class="active-bar" :style="{ width: + barWidth(index) + '%' }"></div>
                    </div>
                    <span>0{{ testimonials.length }}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    background-color: $testimonials-bg;

    .big-container {
        position: relative;
        padding: 140px 0;
        display: flex;
        justify-content: center;
        color: $white;

        .testimonial-content {
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            max-width: 690px;

            img {
                max-width: 120px;
            }

            h2 {
                margin: 25px 0;
                font-size: 22px;
            }

            P {
                color: $text-tertiary;
                margin-bottom: 40px;
            }
        }
    }

    .carousel-bar {
        display: flex;
        align-items: center;

        .bar {
            width: 120px;
            height: 1px;
            background-color: $carousel-bar;
            position: relative;
            margin: 0 15px;
        }

        .active-bar {
            height: 1px;
            background-color: $white;
            position: absolute;
            left: 0;
            top: 0;
        }
    }

}
</style>