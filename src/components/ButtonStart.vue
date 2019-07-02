<template>
  <button class="button" @click="emitClick">
    {{ text }}
  </button>
</template>

<script>

export default {
  name: 'buttonStart',
  props: [
    'text',
  ],
  methods: {
    emitClick() {
      this.$emit('click');
    },
  },
};
</script>

<style scoped lang="scss">
.home {
  &__title {
    font-size: 3rem;
    margin-bottom: 8rem;
  }
}

.button {
  display: flex;
    justify-content: center;
    align-items: center;
    width: 7rem;
    height: 2rem;
    background: #4e9caf;
    text-align: center;
    border-radius: 1rem;
    border: none;
    text-decoration: none;
    color: white;
    font-weight: bold;
    margin: 0 auto;
    cursor: pointer;
}
</style>
