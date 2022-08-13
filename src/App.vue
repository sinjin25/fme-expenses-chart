<template>
    <Card class="final-center">
        <Balance class="card-gap"><Logo /></Balance>
        <ChartCard>
            <template v-slot:head>
                <span style="display: inline-block;"><h2>Spending - Last 7 days</h2></span>
            </template>
            <template v-slot:body>
                <Graph></Graph>
            </template>
            <template v-slot:footer>
                <ChartFooter></ChartFooter>
            </template>
        </ChartCard>
    </Card>
</template>

<script>
import Card from './components/Card.vue'
import Balance from './components/Balance.vue'
import Logo from './components/Logo.vue'
import ChartCard from './components/ChartCard.vue'
import ChartFooter from './components/ChartFooter.vue'
import Graph from './components/Graph.vue'

export default {
  name: 'App',
  components: {
    Card,
    Balance,
    Logo,
    ChartCard,
    ChartFooter,
    Graph,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;700&display=swap');
</style>

<style lang="scss" scoped>
.final-center {
    position: fixed;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}
/* for matching guide against component */
/* .pos-x {
    position: absolute;
    left: 0%;
    top: 0%;
    z-index: 2;
}
.pos-y {
    position: absolute;
    left: 50%;
    top: 0%;
    transform: translate(-50%, -50%);
    z-index: 2;
    &.card {
        padding-top: 0rem!important;
        padding-bottom: 0rem!important;
    }
}
.pos-2-x {
    position: relative;
    left: 25%;
}
.pos-2-y {
    position: relative;
    bottom: 25%;
} */
/* for comparing to picture stuff */
/* .guide-options {
    position: relative;
    > * {
        flex: 0 0 auto;
    }
} */
.card-gap {
    margin-bottom: 1rem;
}
</style>