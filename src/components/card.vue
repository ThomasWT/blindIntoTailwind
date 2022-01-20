<template>
    <div class="card block p-6 w-72 mx-auto rounded-lg m-7">
        <platform :color="data.color" :logo="data.logo" :name="data.name" />
        <stats :change="data.percentChange" :val="data.val" :unit="data.unit" :type="data.type" />
        <chart :weeklyGraph="data.weeklyGraph" />
    </div>
</template>

<script>
import stats from './stats.vue'
import platform from './platform.vue'
import chart from './chart.vue'
    export default {
        props: ['data'],
        components: {
            platform,
            stats,
            chart
        }
    }
</script>

<style lang="scss" scoped>
    .card {
        background: #231E3D;
    }
</style>