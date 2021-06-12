<template>
  <h4>App text</h4>
  <ChildStyles />
</template>

<script>
import ChildStyles from "./components/ChildStyles.vue";

export default {
  name: "App",
  components: {
    ChildStyles,
  },
  data() {
    return {};
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}

h4 {
  color: blue;
}
</style>
