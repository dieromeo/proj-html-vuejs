<script>
export default {
    name: 'Logo',
    data() {
        return {
            logo: { img: "../../../public/img/logo-img-01.png", alt: 'logo' }
        }
    }
}
</script>

<template>
    <!-- logo  -->
    <img :src="logo.img" :alt="logo.alt">
</template>

<style lang="scss" scoped>
img {
    height: 25px;
}
</style>