<template>
  <div class="black-bg" v-if="showModal == true">
    <div class="white-bg">
      <h4>Title</h4>
      <p>Description</p>
    </div>
  </div>
  <div>
    <a class="menu" v-for="menu in menus" :key="menu">{{ menu }}</a>
  </div>
  <div v-for="(product, i) in products" :key="i">
    <img :src="`./assets/room${[i]}.jpg`" alt="" />
    <!-- <img src="./assets/room1.jpg" alt="" /> -->
    <h4 @click="showModal = true">{{ products[i] }}</h4>
    <p>${{ prices[i] }}</p>
    <button @click="increaseCount(i)">Click to Report</button>
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
      showModal: false,
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

body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}

.menu {
  background-color: darkblue;
  color: white;
  padding: 20px;
}
</style>
