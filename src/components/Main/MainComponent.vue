<script>
import Specialties from './Specialties.vue';
import Team from './Team.vue';
import UpcomingEvents from './UpcomingEvents.vue';

export default {
    name: 'MainComponent',
    components: { Specialties, Team, UpcomingEvents }
}
</script>

<template>
    <Specialties />
    <Team />
    <UpcomingEvents />
</template>

<style></style>