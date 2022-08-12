<template>
    <Guide class="--side-by-side guide-options">
        <template #default>
            <Card>
                <Balance class="card-gap"><Logo /></Balance>
                <ChartCard>
                    <template v-slot:head>
                        <h2>Spending - Last 7 Days</h2>
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
        <template #guide>
            <MobileGuide />
        </template>
    </Guide>
</template>

<script>
import Card from './components/Card.vue'
import Guide from './components/Guide.vue'
import MobileGuide from './components/MobileGuide.vue'
import Balance from './components/Balance.vue'
import Logo from './components/Logo.vue'
import ChartCard from './components/ChartCard.vue'
import ChartFooter from './components/ChartFooter.vue'
import Graph from './components/Graph.vue'

export default {
  name: 'App',
  components: {
    MobileGuide,
    Guide,
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
.guide-options {
    > * {
        flex: 0 0 auto;
        /* margin: 0 auto; */
    }
}
.card-gap {
    margin-bottom: 1rem;
}
</style>