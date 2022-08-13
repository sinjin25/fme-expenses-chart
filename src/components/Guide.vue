<template>
    <div id="guide">
        <div>
            <slot></slot>
        </div>
        <div>
            <slot name="guide"></slot>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
#guide {
    &.--side-by-side {
        display: flex;
        flex-direction: row;
    }
    &.--top-down {
        display: flex;
        flex-direction: column;
        text-align: center;
    }
    .ml {
        margin-left: auto;
    }
}
</style>