<script>
import ReadMore from '../ReadMore.vue';
import Form from './Form.vue';

export default {
    name: 'AboutUs',
    data() {
        return {
            mapImage: { url: '../../../public/img/h1-contact-rev-01.png', alt: 'map' },
            plusImage: { url: '../../../public/img/h1-contact-rev-02.png', alt: 'plus' },
            title: 'Contact us',
            subtitle: 'Lorem ispum dolor sit amet, consectetur adipiscing elit',
            logoLIst: [
                { fisrtUrl: '../../../public/img/h4-clients-img-03.png', secondUrl: '../../../public/img/h4-clients-img-04-1.png', alt: 'logo', active: true },
                { fisrtUrl: '../../../public/img/h4-clients-img-05.png', secondUrl: '../../../public/img/h4-clients-img-06-1.png', alt: 'logo', active: true },
                { fisrtUrl: '../../../public/img/h4-clients-img-07.png', secondUrl: '../../../public/img/h4-clients-img-08-1.png', alt: 'logo', active: true },
                { fisrtUrl: '../../../public/img/h4-clients-img-09.png', secondUrl: '../../../public/img/h4-clients-img-10-1.png', alt: 'logo', active: true },
                { fisrtUrl: '../../../public/img/h4-clients-img-01.png', secondUrl: '../../../public/img/h4-clients-img-02.png', alt: 'logo', active: true },
            ]
        };
    },
    components: { ReadMore, Form },
    methods: {
        changeLogo(index) {
            if (this.logoLIst[index].active === true) {
                this.logoLIst[index].active = false;
            } else {
                this.logoLIst[index].active = true;
            }
        }
    }
}
</script>

<template>
    <section>
        <div class="small-container">
            <div class="main-content">
                <!-- parte di sinistra con mappa  -->
                <div class="left">
                    <img :src="mapImage.url" :alt="mapImage.alt">
                    <img class="new-york" :src="plusImage.url" :alt="plusImage.alt">
                    <img class="melbourne" :src="plusImage.url" :alt="plusImage.alt">
                    <img class="london" :src="plusImage.url" :alt="plusImage.alt">
                    <!-- evento  -->
                    <div class="event">
                        <h2>New York Coaching</h2>
                        <ReadMore class="no-mg" />
                    </div>
                </div>
                <!-- parte destra con form  -->
                <div class="right">
                    <Form :titolo="title" :sottotitolo="subtitle" />
                </div>
            </div>
            <ul>
                <li v-for="(logo, index) in logoLIst">
                    <a href="#"><img @mouseenter="changeLogo(index)" @mouseleave="changeLogo(index)"
                            :src="logo.active === true ? logo.fisrtUrl : logo.secondUrl" :alt="logo.alt"></a>
                </li>
            </ul>
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
    align-items: center;

    .left {
        width: 50%;
        position: relative;
        max-height: 316px;

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

ul {
    display: flex;
    justify-content: space-between;
    margin-top: 140px;
}
</style>