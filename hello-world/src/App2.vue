<template>
  <h2 v-if="num === 0">The number is zero</h2>
</template>

<script>
export default {
  name: "App2",
  data() {
    return {
      num: 0,
    };
  },
};
</script>

<style></style>
