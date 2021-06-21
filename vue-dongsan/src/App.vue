<template>
  <div>
    <a class="menu" v-for="menu in menus" :key="menu">{{ menu }}</a>
  </div>
  <div v-for="(product, i) in products" :key="i">
    <h4>{{ products[i] }}</h4>
    <p>${{ prices[i] }}</p>
    <button @click="increaseCount(i)">Report</button>
    <span> Report Count: {{ count[i] }}</span>
    <hr />
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
      prices: [1000, 1200, 900],

      products: ["Chancellor Hall", "Folio", "Sitka"],
      menus: ["Home", "Shop", "About"],
      count: [0, 0, 0],
    };
  },
  methods: {
    increaseCount(x) {
      this.count[x] = this.count[x] + 1;
    },
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

.menu {
  background-color: darkblue;
  color: white;
  padding: 20px;
}
</style>
