<template>
  <div class="players">
    <div class="players players--info">
      <span class="players__nome">Nome do Jogador 1</span>
      <input type="text" v-on:keyup.13="getName">
    </div>
    <div class="players players--info">
      <span class="players__nome">Nome do Jogador 2</span>
      <input type="text" v-on:keyup.13="getName">
    </div>
  </div>
</template>

<script>
export default {
  name: "Players",
  data: {
      value: ''
  },
  methods: {
      getName(event) {
          this.value = event.target.value;
          console.log(this.value)
      }
  }
};
</script>

<style scoped lang="scss">
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
