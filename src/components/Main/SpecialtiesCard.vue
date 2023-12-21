<script>
export default {
    name: 'SpecialtiesCard',
    props: ['immagine', 'titolo', 'contenuto']
}
</script>

<template>
    <div class="card">
        <!-- immagine  -->
        <div class="image-container">
            <img :src="immagine" :alt="titolo">
        </div>
        <!-- titolo e contenuto  -->
        <h2>{{ titolo }}</h2>
        <p>{{ contenuto }}</p>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.card {
    display: flex;
    flex-direction: column;
    align-items: center;

}

h2 {
    margin: 22px 0;
    font-size: 24px;
}

p {
    max-width: 205px;
    color: $text-secondary;
}
</style>