<template>
    <div class="placeholder grid">
        <GraphBar class="grid-bar"
        :class="index === 2 ? '--highlight' : ''"
        :percent="item"
        v-for="(item, index) in bars" :key="index"
        ></GraphBar>
        <GraphLabel class="grid-label"
        v-for="(item, index) in days" :key="index"
        >{{item}}</GraphLabel>
        
    </div>
</template>

<script>
import GraphLabel from './Graph/GraphLabel.vue'
import GraphBar from './Graph/GraphBar.vue'

export default {
    components: {
        GraphLabel,
        GraphBar,
    },
    data() {
        return {
            bars: [
                31,
                62,
                92,
                55,
                42,
                75,
                45
            ],
            days: ['mon', 'tue', 'wed', 'thu', 'fri', 'sat', 'sun']
        }
    }
}
</script>

<style lang="scss" scoped>
.placeholder {
    /* max-height: 217px; */
    border-bottom: 2px solid var(--cream);
}
.grid {
    display: grid;
    /* un-hardcode this */
    grid-template-columns: repeat(7, 1fr);
    grid-template-rows: 165px 49px;
    &-bar {
        padding: 0 .4em;
    }
    @media only screen and (min-width: 768px) {
        padding-top: 1rem;
        grid-template-rows: 165px 45px; // little nudge to the bottom
        padding-bottom: .5rem;
    }
}
</style>