<template>
  <div id="app">
    <git-to-docker/>
  </div>
</template>

<script>
import GitToDocker from "./components/GitToDocker.vue";

export default {
  name: "app",
  components: {
    GitToDocker
  }
};
</script>

<style>
html,
body {
  height: 100%;
  margin: 0px;
  padding: 0px;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100%;
}
</style>
