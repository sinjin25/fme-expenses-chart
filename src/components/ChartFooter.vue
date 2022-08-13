<template>
    <div class="chart-footer">
        <div class="chart-footer-body">
            <h2 class="chart-footer-title"><span>Total this month</span></h2>
            <div class="chart-footer-gains">
                <div class="chart-footer-num">{{balance}}</div>
                <div class="chart-footer-sub">
                    <div class="chart-footer-gain">+2.4%</div>
                    <div class="chart-footer-title --2">from last month</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            balance: '$478.33'
        }
    }
}
</script>

<style lang="scss" scoped>
.chart-footer {
    text-align: left;
    border-radius: 0.5em;
    padding-top: 1.25rem;
    display: flex;
    justify-content: space-between;
    &-body {
        width: 100%;
    }
    &-title {
        font-size: .85rem;
        line-height: 1.5;
        color: var(--medium-brown);
        letter-spacing: -0.03em;
    }
    &-num {
        font-size: 1.6rem;
        font-weight: 700;
        letter-spacing: 0.02em;
        color: var(--dark-brown);
        align-self: flex-end;
    }
    &-sub {
        text-align: right;
    }
    &-gain {
        font-size: .9rem;
        color: var(--dark-brown);
        font-weight: 700;
    }
    &-gains {
        display: flex;
        justify-content: space-between;
        .chart-footer-num {
            margin-right: auto;
        }
    }
    @media only screen and (min-width: 768px) {
        padding-top: 1.8rem;
        padding-bottom: .5rem;
        &-title {
            font-size: 1.1rem;
        }
        &-num {
            font-size: 2.6rem;
        }
        &-gain {
            font-size: 1.1rem;
        }
    }
}
</style>