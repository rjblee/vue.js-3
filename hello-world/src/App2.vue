<template>
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>Not a number</h2>
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
