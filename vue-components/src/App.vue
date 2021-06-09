<template>
  <button @click="showPopup = true">Show Popup</button>
  <Popup v-show="showPopup" @close="showPopup = false" />
</template>

<script>
// import Greet from "./components/Greet.vue";
// import Article from "./components/Article.vue";
import Popup from "./components/Popup.vue";

export default {
  name: "App",
  components: {
    // Greet,
    // Article,
    Popup,
  },
  data() {
    return {
      showPopup: false,
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
