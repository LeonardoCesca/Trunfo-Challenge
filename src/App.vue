<template>
  <div id="app">
    <h1>SuperTrunfo</h1>
    <Players v-model="player"></Players>
    {{player.player1}}
    {{player.player2}}
    <router-view/>
  </div>
</template>

<script>
import Players from '@/components/Players.vue';

export default {
  components: {
    Players,
  },
  data() {
    return {
      player: {
        player1: '',
        player2: '',
      },
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
