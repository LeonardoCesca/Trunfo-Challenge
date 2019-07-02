<template>
  <div class="c-play">
    <span class="c-play__back">
      <router-link to="/">voltar</router-link></span>
    <h1 class="c-play__title">SuperTrunfo</h1>
  </div>
</template>

<script>

export default {
  name: 'game',
};
</script>

<style scoped lang="scss">
.c-play {
  &__back {
    font-size: 1rem;
    margin-bottom: 8rem;
    float: left;
    padding-left: 10px;

    & a {
    text-decoration: none;
    color: #000;

      &:hover {
      text-decoration: underline;
      color:#000;
      transition: 2s;
      }
    }
  }

  &__title {
    font-size: 3rem;
    margin-bottom: 8rem;
  }
}
</style>
