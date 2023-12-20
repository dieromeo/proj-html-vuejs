<script>
import Bar from '../Bar.vue';
import Socials from '../Socials.vue'

export default {
    name: 'TeamCard',
    props: ['titolo', 'sottotitolo', 'paragrafo'],
    components: { Bar, Socials }
}
</script>

<template>
    <div class="card-container">
        <h2>{{ titolo }}</h2>
        <p class="sottotitolo">{{ sottotitolo }}</p>
        <Bar />
        <p class="paragraph">{{ paragrafo }}</p>
        <Socials />
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.card-container {
    padding: 90px 120px 100px 60px;
    max-width: 700px;
    background-color: $white;

    h2 {
        font-size: 40px;
    }

    .sottotitolo {
        margin-bottom: 20px;
        color: $text-secondary;
    }

    .paragraph {
        margin-top: 30px;
        font-size: 19px;
        color: $text-secondary;
    }
}
</style>