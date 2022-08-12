<template>
    <div class="balance">
        <div class="balance-body">
            <h2 class="balance-title">My balance</h2>
            <div class="balance-num">{{balance}}</div>
        </div>
        <!-- icon -->
        <div class="balance-icon">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            balance: '$921.48'
        }
    }
}
</script>

<style lang="scss" scoped>
.balance {
    background: var(--soft-red);
    color: var(--very-pale-orange);
    text-align: left;
    padding: 1em;
    border-radius: 0.5em;
    padding-bottom: 1.3rem;
    display: flex;
    justify-content: space-between;
    &-title {
        font-size: .9rem;
        line-height: 1.5;
    }
    &-num {
        font-size: 1.3rem;
        font-weight: 700;
    }
    &-icon {
        display: flex;
        align-items: center;
    }
}
</style>