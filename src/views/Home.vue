<template>
  <div class="home">
    <h1 class="home__title">SuperTrunfo</h1>
    <Players/>
  </div>
</template>

<script>
import Players from '@/components/Players.vue';

export default {
  name: 'home',
  components: {
    Players,
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
</style>
