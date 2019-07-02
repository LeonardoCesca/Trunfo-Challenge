<template>
  <div class="button">
    <router-link to="/game">Play</router-link>
  </div>
</template>

<script>

export default {
  name: 'home',
};
</script>

<style scoped lang="scss">
.home {
  &__title {
    font-size: 3rem;
    margin-bottom: 8rem;
  }
  a {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 7rem;
    height: 1.5rem;
    background: #4e9caf;
    padding: .7rem;
    text-align: center;
    border-radius: 1rem;
    text-decoration: none;
    color: white;
    font-weight: bold;
    margin: 0 auto;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
