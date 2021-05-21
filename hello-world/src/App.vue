<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 :class="status">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldOut ? 'sold-out' : 'new'">Soldout</h2>
  <h2 :class="['new', 'promoted']">Newly Promoted Movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">
    Array conditional movie
  </h2>
  <h2
    :class="{
      promoted: isPromoted,
      new: !isSoldOut,
      'sold-out': isSoldout,
    }"
  >
    Object conditional movie
  </h2>

  <h2
    :style="{
      color: highlightColor,
      'font-size': headerSize + 'px',
      padding: '20px',
    }"
  >
    Inline style
  </h2>
  <h2 :style="headerStyleObject">Style Object</h2>

  <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
  <div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>

  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      headingId: "heading",
      isDisabled: true,
      status: "success",
      isPromoted: true,
      isSoldOut: true,
      highlightColor: "orange",
      headerSize: 50,
      headerStyleObject: {
        color: "orange",
        fontSize: "50px",
        padding: "20px",
      },
      baseStyleObject: {
        fontSize: "50px",
        padding: "10px",
      },
      successStyleObject: {
        color: "green",
        backgroundColor: "lightgreen",
        border: "1px solid green",
        padding: "20px",
      },
      dangerStyleObject: {
        color: "darkred",
        backgroundColor: "red",
        border: "1px solid darkred",
      },
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

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.sold-out {
  color: red;
}
</style>
