<template>
  <div id="app">
    <h1>SuperTrunfo</h1>
    <Players v-model="player" @input="test"/>
    {{player.player1}}
    {{player.player2}}
    <!-- <router-view/> -->
  </div>
</template>

<script>
import Players from './components/Players.vue';

export default {
  name: 'app',
  components: {
    Players,
  },
  data() {
    return {
      player: {
        player1: 'dasdasd',
        player2: 'dasdda',
      },
    };
  },
  methods: {
    test() {
      console.log('oi');
    }
  }
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
