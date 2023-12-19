<script>
export default {
    name: 'SpecialtiesCard',
    props: ['immagine', 'titolo', 'contenuto']
}
</script>

<template>
    <div class="image-container">
        <img :src="immagine" :alt="titolo">
    </div>
    <h2>{{ titolo }}</h2>
    <p>{{ contenuto }}</p>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

h2 {
    margin: 22px 0;
    font-size: 24px;
}

p {
    max-width: 205px;
    color: $text-secondary;
}
</style>