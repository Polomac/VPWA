<template>
  <div class="home-wrapper">
    <h1>This is home page</h1>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      msg: 'Welcome to Your Vue.js PWA',
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/default';

.home-wrapper {
  padding: 0.625em;
  min-height: 74vh;
}
</style>
