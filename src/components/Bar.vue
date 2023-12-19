<script>
export default {
    name: 'Bar'
}
</script>

<template>
    <div class="bar">
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.bar {
    background-color: $secondary-color;
    height: 2px;
    width: 70px;
}
</style>