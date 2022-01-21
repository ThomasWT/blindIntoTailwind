<template>
  <div id="app">
    <card :data="platform" v-for="platform in platforms" :key="platform.name" />
  </div>
</template>

<script>
  import card from './components/card.vue'
  export default {
    name: 'App',
    components: {
      card
    },
    data() {
      return {
        platforms: [{
            name: 'YouTube',
            val: 1.2,
            unit: 'm',
            type: 'followers',
            percentChange: 2.2,
            weeklyGraph: [7, 9, 7.5, 9, 8.5, 10],
            logo: 'youtube.svg',
            color: '#C8102E'
          },
          {
            name: 'Twitch',
            val: 300,
            unit: '',
            type: 'subscribers',
            percentChange: 8.3,
            weeklyGraph: [9, 5, 7.5, 6, 8.5, 10],
            logo: 'icon_tw.svg',
            color: '#9146FF'
          },
        ]
      }
    }
  }
</script>

<style lang="scss">
  html {
    background: #1A162F;
  }
  #app {
    font-family: 'Poppins';
    margin-top: 60px;
  }
</style>
