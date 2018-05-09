<template>
  <div class="footer-wrapper">
    <h1>PWA template</h1>
  </div>
</template>

<script>
export default {
  name: 'footer-component',
  data() {
    return {
    };
  },
};
</script>


<style lang="scss" scoped>
@import '../../assets/styles/default';

.footer-wrapper {
  height: 200px;
  background: $primary;
  color: $inverted;
  padding: 1em;
}
</style>
