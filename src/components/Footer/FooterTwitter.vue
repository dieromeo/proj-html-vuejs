<script>
import FooterBar from './FooterBar.vue';

export default {
    name: 'FooterTwitter',
    data() {
        return {
            title: 'Twitter',
            firstContent: '@HenrySefaBoaky1 Check out our theme Gioia which has all necessary elements to build a multi vendor marketplace. https://t.co/c9BIYxZBIL',

        };
    },
    components: { FooterBar }
}
</script>

<template>
    <div>
        <h2>{{ title }}</h2>
        <FooterBar />
        <div class="first">
            <font-awesome-icon icon="fa-brands fa-twitter" />
            <div class="text">
                <a href="#">@aliasadadm</a>
                <span> Hi </span>
                <a href="#">@aliasadadm</a>
                <span>, can you please submit a ticket at </span>
                <a href="#">https://t.co/JLV61aXG7d</a>
                <span> and one of our support agent ... </span>
                <a href="#">https://t.co/yk57k159bS</a>
            </div>
        </div>
        <div class="second">
            <font-awesome-icon icon="fa-brands fa-twitter" />
            <div class="text">
                <a href="#">@HenrySefaBoaky1</a>
                <span> Check out our theme Gioia which has all necessary elements to build a multi vendor marketplace.
                </span>
                <a href="#">https://t.co/c9BIYxZBIL</a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
a {
    text-decoration: underline;
    color: currentColor;
}

.first,
.second {
    display: flex;

    .text {
        margin-left: 24px;
        margin-bottom: 10px;
    }
}
</style>