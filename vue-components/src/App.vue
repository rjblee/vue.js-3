<template>
  <Input v-model="name" />
  <h2>{{ name }}</h2>
</template>

<script>
// import Greet from "./components/Greet.vue";
// import Article from "./components/Article.vue";
// import Popup from "./components/Popup.vue";
import Input from "./components/Input.vue";

export default {
  name: "App",
  components: {
    Input,
  },
  data() {
    return {
      name: "",
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
  margin-top: 60px;
}
</style>
