<template>
  <section class="player">
  <div class="players">
    <div class="players players--info">
      <span class="players__nome">Nome do Jogador 1</span>
      <input type="text" ref="player1" :value="value.player1" @input="getName()">
      {{value.player1}}
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
  props: {
    value: {
      type: Object,
    },
  },
  created() {
    console.log(this.value);
  },
  methods: {
    getName() {
      this.$emit('input', {
        player1: this.$refs.player1.value,
        player2: this.$refs.player2.value,
      });
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
