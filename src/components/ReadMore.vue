<script>
export default {
    name: 'ReadMore',
    data() {
        return {
            content: 'read more'
        }
    }
}
</script>

<template>
    <h3>{{ content.toUpperCase() }}</h3>
</template>

<style lang="scss" scoped>
h3 {
    margin-top: 20px;
    font-size: 14px;
    cursor: pointer;
}
</style>