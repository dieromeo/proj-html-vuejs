<script>
import BottomArrow from './components/BottomArrow.vue';
import FooterComponent from './components/Footer/FooterComponent.vue';
import HeaderComponent from './components/Header/HeaderComponent.vue';
import MainComponent from './components/Main/MainComponent.vue';

export default {
    components: { HeaderComponent, MainComponent, FooterComponent, BottomArrow }
}
</script>

<template>
    <BottomArrow />
    <HeaderComponent />
    <MainComponent />
    <FooterComponent />
</template>

<style lang="scss">
@use './style/main.scss'
</style>