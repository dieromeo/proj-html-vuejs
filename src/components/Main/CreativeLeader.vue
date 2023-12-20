<script>
import Bar from '../Bar.vue';
import ReadMore from '../ReadMore.vue';

export default {
    name: 'CreativeLeader',
    data() {
        return {
            title: 'Creative Leader',
            content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do nulla eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut etim enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. SDuis aute irure dolor in sociis.',
            bars: [
                { title: 'Mentorship', width: '78%' },
                { title: 'Education', width: '95%' },
                { title: 'Learning', width: '65%' },
                { title: 'Motivation', width: '83%' },
            ],
        };
    },
    components: { Bar, ReadMore }
}
</script>

<template>
    <section>
        <div class="small-container">
            <div class="left">
                <h2> {{ title }}<span class="dot">.</span></h2>
                <Bar />
                <p>{{ content }}</p>
                <ReadMore />
            </div>
            <div class="right">
                <div v-for="bar in bars">
                    <div class="info-percentuale">
                        <h2>{{ bar.title }}</h2>
                        <span>{{ bar.width }}</span>
                    </div>
                    <div class="percentuale">
                        <div class="completed" :style="{ width: bar.width }"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    padding: 130px 0 140px 0;

    .small-container {
        display: flex;
        gap: 85px;
    }

    .left {
        max-width: 50%;

        h2 {
            font-size: 32px;
            margin-bottom: 20px;
        }

        p {
            margin-top: 20px;
            color: $text-secondary;
            font-size: 18px;
        }
    }

    .right {
        .percentuale {
            width: 635px;
            height: 4px;
            border-bottom: 1px solid $text-secondary;
            position: relative;
            margin-bottom: 30px;
        }

        .completed {
            background-color: $secondary-color;
            height: 4px;
            position: absolute;
            top: 0;
            left: 0;
        }

        .info-percentuale {
            display: flex;
            justify-content: space-between;

            h2 {
                margin-bottom: 15px;
                font-size: 20px;
            }

            span {
                font-weight: bold;
            }
        }
    }
}
</style>