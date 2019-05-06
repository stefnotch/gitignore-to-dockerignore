<template>
  <div class="flex-row-container">
    <textarea v-model="gitignore"></textarea>
    <pre><code>{{ gitToDocker(gitignore) }}</code></pre>
  </div>
</template>

<script>
import gitignoreToDockerignore from "gitignore-to-dockerignore";

export default {
  name: "git-to-docker",
  data() {
    return {
      gitignore: ""
    };
  },
  methods: {
    gitToDocker(text) {
      return gitignoreToDockerignore(text);
    }
  }
};
</script>
<style scoped>
.flex-row-container {
  display: flex;
  flex-direction: row;
  height: 100%;
}

.flex-row-container > * {
  flex: 1;
  background-color: #eeeeee;
  margin: 24px;
  padding: 0px;
  height: calc(100vh - 48px);
  overflow-y: auto;
}
</style>

