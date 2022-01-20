<template>
    <div :style="{background: color}" class="platformContainer mb-6 w-fit pt-2 pb-2 rounded-md flex">
        <div class="logoContainer max-h-0.5  ml-3 inline-block">
            <img class="h-4" :src="require(`@/assets/socialmedia/logos/${logo}`)">
        </div>
        <div class="platform h-4 ml-2 font-semibold text-xs leading-5 text-white items-center flex mr-3">
            {{name}}
        </div>
    </div>
</template>

<script>
export default {
    props: ['logo', 'name', 'color'],
}
</script>