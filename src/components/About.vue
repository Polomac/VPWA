<template>
  <div class="about-wrapper">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'about',
  data() {
    return {
      msg: 'This is \'About\' page',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import '../assets/styles/default';

.about-wrapper {
  padding: 0.625em;
  min-height: 74vh;
}
</style>
