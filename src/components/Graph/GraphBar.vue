<template>
    <div class="bar-container">
        <div class="bar"
        :style="style"></div>
    </div>
</template>

<script>
export default {
    props: ['percent'],
    computed: {
        style() {
            return `height: ${this.percent}%;`
        }
    }
}
</script>

<style lang="scss" scoped>
.bar {
    background-color: var(--soft-red);
    flex: 1 auto;
    border-radius: 0.25em;
    &-container {
        display: flex;
        height: 100%;
        align-items: flex-end;
    }
}
/* blue bar */
.bar-container.--highlight {
    .bar {
        background-color: var(--cyan);
    }
}
</style>