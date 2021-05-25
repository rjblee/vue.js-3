<template>
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else>The number is NOT zero</h2>
</template>

<script>
export default {
  name: "App2",
  data() {
    return {
      num: 1,
    };
  },
};
</script>

<style></style>
