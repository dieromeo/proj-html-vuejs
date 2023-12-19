<script>
import Logo from './Logo.vue';
import Navbar from './Navbar.vue';

export default {
    name: 'Topbar',
    components: { Logo, Navbar }
}
</script>

<template>
    <div class="top-bar">
        <Logo />
        <Navbar />
    </div>
</template>

<style lang="scss" scoped>
.top-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 45px 0;
}
</style>