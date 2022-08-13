<template>
    <div class="chart">
        <div class="chart-head">
            <slot name="head"></slot>
        </div>
        <div class="chart-body">
            <slot name="body"></slot>
        </div>
        <div class="chart-footer">
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.chart {
    padding: 1.5em 1em;
    background: var(--very-pale-orange);
    border-radius: 0.5em;
    &-head {
        font-size: 1.25rem;
        font-weight: 700;
        margin-bottom: 2rem;
        text-align: left;
        color: var(--dark-brown);
    }
    &-body {
        margin: 0 -.25em;
    }
    &-footer {}
    @media only screen and (min-width: 768px) {
        padding: 1.7em 2em;
        /* height: 510px; */
        &-head {
            font-size: 1.8rem;
        }
    }
}
</style>