<script>
import ReadMore from '../ReadMore.vue';

export default {
    name: 'AboutUs',
    data() {
        return {
            mapImage: { url: '../../../public/img/h1-contact-rev-01.png', alt: 'map' },
            plusImage: { url: '../../../public/img/h1-contact-rev-02.png', alt: 'plus' }
        };
    },
    components: { ReadMore }
}
</script>

<template>
    <section>
        <div class="small-container">
            <div class="main-content">
                <div class="left">
                    <img :src="mapImage.url" :alt="mapImage.alt">
                    <img class="new-york" :src="plusImage.url" :alt="plusImage.alt">
                    <img class="melbourne" :src="plusImage.url" :alt="plusImage.alt">
                    <img class="london" :src="plusImage.url" :alt="plusImage.alt">
                    <div class="event">
                        <h2>New York Coaching</h2>
                        <ReadMore class="no-mg" />
                    </div>
                </div>
                <div class="right"></div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.small-container {
    padding: 120px 0 150px 0;
}

.main-content {
    display: flex;
    gap: 70px;

    .left {
        width: 50%;
        position: relative;

        .new-york {
            position: absolute;
            bottom: 180px;
            left: 138px;
        }

        .melbourne {
            position: absolute;
            left: 488px;
            bottom: 64px;
        }

        .london {
            position: absolute;
            left: 304px;
            top: 70px;
        }

        .event {
            padding: 20px 42px 25px 30px;
            background-color: $white;
            box-shadow: 1px 1px 1px 1px $text-secondary;
            position: absolute;
            left: 128px;
            bottom: 72px;

            h2 {
                font-size: 20px;
                margin-bottom: 10px;
            }

            .no-mg {
                margin: 0;
            }
        }
    }

    .right {
        width: 50%;
    }
}
</style>