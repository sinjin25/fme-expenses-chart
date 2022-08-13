<template>
    <div class="label">
        <span><slot></slot></span>
    </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
.label {
    font-size: .7rem;
    color: var(--medium-brown);
    display: flex;
    justify-content: center;
    align-items: center;
    padding-bottom: .7rem;
    @media only screen and (min-width: 768px) {
        font-size: .75rem;
    }
}
</style>