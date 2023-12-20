<script>
import Carousel from './Carousel.vue';
import CreativeLeader from './CreativeLeader.vue';
import LatestNews from './LatestNews.vue';
import Specialties from './Specialties.vue';
import Team from './Team.vue';
import Testimonials from './Testimonials.vue';
import UpcomingEvents from './UpcomingEvents.vue';

export default {
    name: 'MainComponent',
    components: { Specialties, Team, UpcomingEvents, CreativeLeader, LatestNews, Testimonials, Carousel }
}
</script>

<template>
    <Specialties />
    <Team />
    <UpcomingEvents />
    <CreativeLeader />
    <LatestNews />
    <Testimonials />
    <Carousel />
</template>

<style></style>