<script>
import SmallRightArrow from './SmallRightArrow.vue'

export default {
    name: 'MainButton',
    props: ['testoBottone'],
    components: { SmallRightArrow }
}
</script>

<template>
    <button>
        <div class="button-text">
            <h5>{{ testoBottone.toUpperCase() }}</h5>
        </div>
        <div class="arrow">
            <SmallRightArrow />
        </div>
    </button>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

button {
    display: flex;
    align-items: center;
    padding: 11px 0;
    background-color: $white;
    font-size: 12px;
    cursor: pointer;

    div.button-text {
        padding: 10px 35px;
        border-right: 1px solid currentColor;
    }

    .arrow {
        padding: 0 15px;
    }
}
</style>