<template>
  <!-- <Greet name="Ralph" heroName="Spiderman" />
  <Greet name="Andy" heroName="Batman" />
  <Greet name="Tommy" heroName="Superman" /> -->

  <Article
    id="my-article"
    title="Article Title"
    :likes="50"
    :isPublished="true"
  ></Article>
</template>

<script>
// import Greet from "./components/Greet.vue";
import Article from "./components/Article.vue";

export default {
  name: "App",
  components: {
    // Greet,
    Article,
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
