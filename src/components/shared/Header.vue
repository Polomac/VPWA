<template>
  <div class="header-wrapper">
    <div class="branded">
      <i class="material-icons hamburger"
         @click="toggleNavVert">menu</i>
      <span class="brand-label">PWA Template</span>
    </div>
    <div class="nav-dt">
      <router-link to="home">Home</router-link>
      <router-link to="about">About</router-link>
    </div>
    <div class="nav-vert"
         :class="{ 'opened': isOpened }"
         @click="toggleNavVert">
      <router-link to="home">
        <i class="material-icons vert">home</i>
        Home
      </router-link>
      <router-link to="about">
        <i class="material-icons vert">help</i>
        About
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'header-component',
  data() {
    return {
      isOpened: false,
    };
  },
  methods: {
    toggleNavVert() {
      this.isOpened = !this.isOpened;
    },
  },
};
</script>

<style lang="scss" scoped>
@import '../../assets/styles/default';

.header-wrapper {
  display: flex;
  padding: 1em;
  background: darken($primary, 50%);
  color: $inverted;
  justify-content: space-between;

  .hamburger {
    align-self: center;
    vertical-align: top;
    padding: 0.125em;
    border-radius: 50%;
    cursor: pointer;
    transition: all 0.3s linear;

    &:hover {
      color: darken($primary, 5%);
    }

    &:active {
      color: $primary;
      background: lighten($primary, 5%);
    }

    @include mqMin(768px) {
      display: none;
    }
  }

  .brand-label {
    font-size: 1.1em;
    font-weight: bold;
    padding: 0 1em;
  }

  .nav-dt {
    display: none;
    padding-right: 1em;
    a {
      color: $inverted;
      text-decoration: none;
      padding: 1em;
      transition: background 0.3s linear;

      &:active {
      color: $primary;
      background: lighten($primary, 5%);
      }
    }
    .router-link-active {
      font-weight: bold;
    }

    @include mqMin(768px) {
      display: block;
    }
  }

  .nav-vert {
    position: absolute;
    top: 56px;
    left: 0;
    height: calc(100% - 60px);
    width: 0px;
    overflow: hidden;
    background: darken($primary, 5%);
    transition: all 0.3s linear;

    a {
      color: $inverted;
      text-decoration: none;
      padding: 1em;
      padding-left: 4em;
      transition: background 0.3s linear;
      display: block;

      &:active {
      color: $primary;
      background: lighten($primary, 5%);
      }
    }

    .router-link-active {
      font-weight: bold;
    }

    .vert {
      margin-top: -1px;
      vertical-align: top;
      left: 0.625em;
      position: absolute;
    }
  }

  .opened {
    width: 300px;
  }
}
</style>
