<template>
  <section class="player">
  <div class="players">
    <div class="players players--info">
      <span class="players__nome">Nome do Jogador 1</span>
      <input type="text" v-model="player1" @input="captureName" >
    </div>
  </div>
    <ButtonStart @click="getName()" text="Play"/>
  </section>
</template>

<script>
import Bus from '../bus';
import ButtonStart from '@/components/ButtonStart.vue';

export default {
  name: 'Players',
  components: {
    ButtonStart,
  },
  data() {
    return {
      player1: '',
    }
  },
  methods: {
    captureName() {
      Bus.$emit('input', this.player1);
    }
  }
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
