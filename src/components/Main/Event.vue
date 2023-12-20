<script>
import ReadMore from '../ReadMore.vue';

export default {
    name: 'Event',
    props: ['data', 'titolo', 'time', 'luogo',],
    components: { ReadMore }
}
</script>

<template>
    <div class="event">
        <div class="data">
            <h3>{{ data.day }}</h3>
            <p>{{ data.month }} {{ data.year }}</p>
        </div>
        <div class="info">
            <h2>{{ titolo }}</h2>
            <div class="time">
                <font-awesome-icon icon="fa-regular fa-clock" />
                <p>{{ time }}</p>
            </div>
            <div class="luogo">
                <font-awesome-icon :icon="['fas', 'location-dot']" />
                <p>{{ luogo }}</p>
            </div>
            <ReadMore />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

.event {
    display: flex;

    box-shadow: 0 0 1px 0 $text-secondary;

    .data {
        padding: 10px;
        background-color: $secondary-color;
        text-align: center;
        color: $white;
        margin-right: 25px;
        max-height: 55px;
    }

    .info {
        h2 {
            margin-bottom: 15px;
            font-size: 18px;
        }

        .time,
        .luogo {
            margin-bottom: 10px;
            color: $text-secondary;
            font-size: 16px;
            display: flex;
        }

        svg {
            margin-right: 12px;
            color: $secondary-color;
        }
    }
}
</style>