<template>
  <div id="app">
    <h1>SuperTrunfo</h1>
    <Players />
    <Game />
    <!-- <router-view/> -->
  </div>
</template>

<script>
import Players from './components/Players.vue';
import Game from './components/Game.vue';

export default {
  name: 'app',
  components: {
    Players,
    Game
  },
  data() {
    return {
      player1: '',
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
