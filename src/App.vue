<template>
  <div id="nav">
    <router-link to="/characters">Characters</router-link> |
    <router-link to="/episodes">Episodes</router-link>
  </div>
  <router-view />
  <br />
  <nav>
    <!-- <router-link :to="prevComp">Prev</router-link> |
    <router-link :to="nextComp">Next</router-link>  -->
  </nav>
</template>

<script>
import {  provide, ref } from 'vue';
export default {
  setup() {
    const info = ref({
      count: 0,
      pages: 0,
      next: 0,
      pev: 0,
    });

    provide("info", info);
    // const route = useRoute();

    // const prevComp = computed(() => ({
    //   name: route.name,
    //   params: { page: info.value.prev || route.params.page },
    // }));

    // const nextComp = computed(() => ({
    //   name: route.name,
    //   params: { page: info.value.next || route.params.page },
    // }));

    return {
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
