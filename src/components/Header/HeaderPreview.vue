<script>
export default {
    name: 'HeaderPreview',
    props: ['titolo', 'contenuto']
}
</script>

<template>
    <div class="info">
        <h1>{{ titolo }}<span>.</span></h1>
        <p>{{ contenuto }}</p>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables.scss' as *;

.info {
    margin-top: 300px;
    margin-left: 220px;
    max-width: 600px;

    h1 {
        font-size: 70px;
    }

    p {
        font-size: 20px;
        margin-top: 30px;
        color: $text-secondary;
    }
}
</style>