<script>
import SmallRightArrow from '../SmallRightArrow.vue';
import SmallLeftArrow from '../SmallLeftArrow.vue'
import TeamCard from './TeamCard.vue';

export default {
    name: 'Team',
    components: { SmallRightArrow, SmallLeftArrow, TeamCard },
    data() {
        return {
            image: { url: '../../../public/img/h1-img-01.jpg', alt: 'Jason Bickford' }
        }
    }
}
</script>

<template>
    <section>
        <div class="team big-container">
            <div class="small-container">
                <div class="image-container">
                    <img :src="image.url" :alt="image.alt">
                    <div class="arrows">
                        <SmallLeftArrow />
                        <SmallRightArrow />
                    </div>
                    <div class="cards-container">
                        <TeamCard />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

section {
    background-color: $team-bg;
    position: relative;
}

.team {
    background-image: url('../../../public/img/svg-4.svg');
    background-repeat: no-repeat;
    background-position-x: 98%;
    background-position-y: 15%;

    .small-container {
        padding: 140px 0;
    }

    .image-container {
        width: 700px;
        position: relative;

        img {
            width: 100%;
            display: block;
        }
    }
}

.arrows {
    display: flex;
    gap: 10px;
    position: absolute;
    left: 0;
    bottom: 0;
    background-color: $secondary-color;
    color: $white;
    padding: 22px 25px;
}
</style>