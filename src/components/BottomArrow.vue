<script>
export default {
    name: 'BottomArrow',
    data() {
        return {
            active: false
        };
    },
    // aggiunta del metodo allo scroll di window
    mounted() {
        window.addEventListener('scroll', this.setScroll);
    },

    methods: {
        // imposta i pixel scrollati
        setScroll() {
            this.active = window.scrollY;
        },
        // fa ritornare la pagina in cima
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }
    }
};
</script>

<template>
    <div class="scroll-to-top" v-if="active" @click="scrollToTop">
        <span class="arrow-up">&ShortUpArrow;</span>
    </div>
</template>
  

  
<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.scroll-to-top {
    position: fixed;
    bottom: 20px;
    right: 0;
    z-index: 999;
    cursor: pointer;
    background-color: $white;
    color: $secondary-color;
    border: 1px solid $text-secondary;
    border-radius: 50%;
    width: 45px;
    height: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.arrow-up {
    font-size: 24px;
}
</style>