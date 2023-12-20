<script>
import Event from './Event.vue';

export default {
    name: 'UpcomingEvents',
    components: [Event],
    data() {
        return {
            title: 'Upcoming events',
            events: [
                {
                    date: { day: '07', month: 'Jan', year: '2022' },
                    title: 'Melbourne Coaching',
                    time: '9:00 am - 5:00 pm, Jan 7, 2022',
                    location: 'Cambridge, MA 02138, USA',
                    more: 'Read more'
                },
                {
                    date: { day: '11', month: 'Jan', year: '2022' },
                    title: 'New York Coaching',
                    time: '9:00 am - 5:00 pm, Jan 11, 2022',
                    location: 'Cambridge, MA 02138, USA',
                    more: 'Read more'
                },
                {
                    date: { day: '21', month: 'Jan', year: '2022' },
                    title: 'London Coaching',
                    time: '9:00 am - 5:00 pm, Jan 21, 2022',
                    location: 'Cambridge, MA 02138, USA',
                    more: 'Read more'
                }
            ]
        };
    },
    components: { Event }
}
</script>

<template>
    <section>
        <div class="small-container">
            <div class="events-container">
                <div class="title">
                    <h2>{{ title }}</h2>
                </div>
                <ul>
                    <li v-for="event in events">
                        <Event :data="event.date" :titolo="event.title" :time="event.time" :luogo="event.location"
                            :more="event.more" />
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    background-image: url('../../../public/img/h1-img-09.jpg');
    padding: 195px 0;

    .events-container {
        background-color: $white;
        max-width: 520px;

        div {
            padding: 25px 50px;
        }
    }

    .title {
        box-shadow: 0px 0px 3px 0px $text-secondary;

        h2 {
            font-size: 28px;
        }
    }
}
</style>