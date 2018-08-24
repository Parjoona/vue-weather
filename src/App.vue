<template>
  <div id="app">
      <app-header></app-header>
        <transition name="slidein" mode="out-in">
          <router-view></router-view>
        </transition>
  </div>
</template>

<script>
  import Header from "./components/Header/Header.vue";

  export default {
    components: {
      appHeader: Header
    }
  }
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.slidein-enter-active, .slidein-leave-active {
  transition: all 250ms;
}
.slidein-enter {
  opacity: 1;
  transform: translate(100%, 0);
}

.slidein-leave-to {
  opacity: 0;
  transform: translate(-100%, 0);
}
</style>
