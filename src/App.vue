<template>
  <div id="app">
    <header-component></header-component>
    <main>
      <router-view></router-view>
    </main>
    <footer-component></footer-component>
  </div>
</template>

<script>
import Header from './components/shared/Header';
import Footer from './components/shared/Footer';

export default {
  name: 'app',
  components: {
    'header-component': Header,
    'footer-component': Footer,
  },
};
</script>

<style lang="scss">
@import '../src/assets/styles/default';
</style>
