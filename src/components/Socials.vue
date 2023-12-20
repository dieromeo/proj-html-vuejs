<script>
import Twitter from './Twitter.vue';

export default {
    name: 'Socials',
    components: { Twitter }
}
</script>

<template>
    <ul>
        <li>
            <div>
                <font-awesome-icon icon="fa-brands fa-linkedin-in" />
            </div>
        </li>
        <li>
            <div>
                <font-awesome-icon icon="fa-brands fa-facebook-f" />
            </div>
        </li>
        <li>
            <Twitter />
        </li>
    </ul>
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

ul {
    display: flex;
    margin-top: 20px;
    gap: 10px;
    color: $white;
}
</style>