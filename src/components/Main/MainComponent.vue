<script>
import CreativeLeader from './CreativeLeader.vue';
import Specialties from './Specialties.vue';
import Team from './Team.vue';
import UpcomingEvents from './UpcomingEvents.vue';

export default {
    name: 'MainComponent',
    components: { Specialties, Team, UpcomingEvents, CreativeLeader }
}
</script>

<template>
    <Specialties />
    <Team />
    <UpcomingEvents />
    <CreativeLeader />
</template>

<style></style>