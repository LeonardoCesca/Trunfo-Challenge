<template>
  <section class="player">
  <div class="players">
    <div class="players players--info">
      <span class="players__nome">Nome do Jogador 1</span>
      <input type="text" v-model="player1">
    </div>
    <div class="players players--info">
      <span class="players__nome">Nome do Jogador 2</span>
      <input type="text" v-model="player2">
    </div>
  </div>
    <ButtonStart @click="getName()" text="Play"/>
  </section>
</template>

<script>
import ButtonStart from '@/components/ButtonStart.vue';

export default {
  name: 'Players',
  components: {
    ButtonStart,
  },
  data() {
    return {
      player1: '',
      player2: '',
    };
  },
  mounted() {
    this.player1 = localStorage.player1;
    this.player2 = localStorage.player2;
  },
  watch: {
    player1(newPlayer) {
      localStorage.player1 = newPlayer;
    },
    player2(newPlayer) {
      localStorage.player2 = newPlayer;
    },
  },
  methods: {
    getName() {
      console.log(this.player1);
      console.log(this.player2);
      this.$router.push({ path: '/game' });
    },
  },
};
</script>

<style scoped lang="scss">
.player {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}

.players {
  display: flex;
  justify-content: space-evenly;
  margin-bottom: 3rem;

  &--info {
    flex-direction: column;
    align-items: flex-start;
  }

  &__nome {
    margin-bottom: 0.1rem;
    font-weight: 600;
  }
}
</style>
