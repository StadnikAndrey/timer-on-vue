<template>
  <div id="app">
    <h1 class="title">"And We Knew It Was Our Time...""</h1>
    <TimeWorld v-for="(time, keys) of timers" :key="keys" :region="time.region" :utc="time.utc" />
  </div>
</template>

<script>
import TimeWorld from './components/TimeWorld.vue'

export default {
  name: 'App',
  data() {
    return {
      timers: [
        { region: 'Coordinated Universal Time (UTC): ', utc: 0 },
        { region: 'Ukraine, Kyiv (+2 hours): ', utc: 120 },
        { region: 'USA, Cleveland (-5 hours): ', utc: -300 },
        { region: 'Japan, Tokyo (+9 hours): ', utc: 540 },
        { region: 'United Kingdom , London (0 hours): ', utc: 0 },
        { region: 'Australia, Sydney (+11 hours): ', utc: 660 }
      ]
    }
  },
  components: {
    TimeWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.title {
  color: coral;
}
</style>
