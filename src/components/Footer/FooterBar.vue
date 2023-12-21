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
@use '../../style/partials/variables' as *;

.bar {
    background-color: $secondary-color;
    height: 1px;
    width: 30px;
    margin: 20px 0;
}
</style>