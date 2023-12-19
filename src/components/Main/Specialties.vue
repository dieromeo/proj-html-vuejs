<script>
import Bar from '../Bar.vue';

export default {
    name: 'Specialties',
    data() {
        return {
            title: 'Our specialties',
            content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit'
        };
    },
    components: { Bar }
}
</script>

<template>
    <section class="big-container">
        <div class="specialties-content">
            <h2>{{ title }}<span class="dot">.</span></h2>
            <p>{{ content }}</p>
            <Bar />
        </div>
        <ul>
            <li></li>
        </ul>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    text-align: center;
    position: relative;

    .specialties-content {
        display: flex;
        flex-direction: column;
        align-items: center;
        position: absolute;
        z-index: 10;
        background-color: $white;
        top: -75px;
        left: 0;
        right: 0;

        h2 {
            font-size: 37px;
            margin-top: 130px;
        }

        p {
            color: $text-secondary;
            margin: 15px 0 30px 0;
        }

        ul {
            margin-top: 70px;
        }
    }
}
</style>