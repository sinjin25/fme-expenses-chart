<template>
    <div class="card">
        <slot></slot>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.card {
    padding: 3.75em 1em;
    /* lol */
    padding-bottom: 3.4em;
    width: 375px;
    background: var(--cream);
    @media only screen and (min-width: 768px) {
        padding: 10rem 1em;
        width: 575px;
    }
}
</style>