<template>
  <router-view v-if="isRouterAlive" />
</template>

<script>
export default {
  name: 'App',

  data() {
    return {
      isRouterAlive: true
    };
  },

  provide() {
    return {
      reload: this.reload
    };
  },

  methods: {
    reload() {
      this.isRouterAlive = false;
      this.$nextTick(() => {
        this.isRouterAlive = true;
      });
    }
  }
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
