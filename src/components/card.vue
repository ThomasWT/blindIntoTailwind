<template>
    <div class="card block p-6 w-72 mx-auto">
        <platform />
    </div>
</template>

<script>
import platform from './platform.vue'
    export default {
        components: {
            platform
        }
    }
</script>

<style lang="scss" scoped>
    .card {
        background: #231E3D;
        border-radius: 20px;
    }
    .platform {
        font-family: 'Poppins';
    }
    .youtube {
        background:#C8102E;
    }
</style>