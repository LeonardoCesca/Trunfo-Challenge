<template>
  <h1>{{ player1 }}</h1>
</template>

<script>
import Bus from '../bus';
import Players from './Players';

export default {
  components: {
    Players,
  },
  data() {
    return {
      player1: '',
    }
  },
  mounted() {
    Bus.$on('input', (value) => this.player1 = value);
  }
};
</script>

<style scoped lang="scss">

</style>
