<template>
    <div class="stats text-left">
        <p class="stat font-bold text-white text-2xl inline-block">{{val}}{{unit}}</p>
        <p class="percentChange inline-block text-xs font-bold align-top mt-2"><span class="ml-3">+ </span>{{change}}%</p>
        <p class="dataType text-left text-sm font-medium">{{type}}</p>
    </div>
</template>
<script>
export default {
    props: ['change', 'val', 'unit', 'type']
}
</script>
<style lang="scss" scoped>
    .stats {
        font-family: 'Poppins';
        .percentChange {
            color:#34C66E;
        }
        .dataType {
            color: #FFFFFF;
        }
    }
</style>