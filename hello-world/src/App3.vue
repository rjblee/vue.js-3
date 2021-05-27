<template>
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
</template>

<script>
export default {
  data() {
    return {
      names: ["Ralph", "Clark", "Michelle"],
    };
  },
};
</script>

<style></style>
