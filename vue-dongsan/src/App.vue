<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h2>Vue Dongsan</h2>
  <div>
    <h4>{{ products[0] }}</h4>
    <p>${{ price1 }}</p>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>${{ price2 }}</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>${{ price3 }}</p>
  </div>
  <hr />
  <div>
    <h4 v-for="product in products">{{ product }}</h4>
    <p>${{ price3 }}</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>${{ price3 }}</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>${{ price3 }}</p>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
  },
  data() {
    return {
      price1: 1000,
      price2: 1200,
      price3: 900,
      products: ["Chancellor Hall", "Folio", "Sitka"],
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
