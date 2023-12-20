<script>
export default {
    name: 'Twitter'
}
</script>

<template>
    <div>
        <font-awesome-icon icon="fa-brands fa-twitter" />
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

div {
    width: 23px;
    height: 23px;
    background-color: $secondary-color;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>