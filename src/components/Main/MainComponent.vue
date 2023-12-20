<script>
import CreativeLeader from './CreativeLeader.vue';
import LatestNews from './LatestNews.vue';
import Specialties from './Specialties.vue';
import Team from './Team.vue';
import UpcomingEvents from './UpcomingEvents.vue';

export default {
    name: 'MainComponent',
    components: { Specialties, Team, UpcomingEvents, CreativeLeader, LatestNews }
}
</script>

<template>
    <Specialties />
    <Team />
    <UpcomingEvents />
    <CreativeLeader />
    <LatestNews />
</template>

<style></style>