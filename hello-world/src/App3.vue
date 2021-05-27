<template>
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
</template>

<script>
export default {
  data() {
    return {
      names: ["Ralph", "Clark", "Michelle"],
      fullNames: [
        { first: "Ralph", last: "Lee" },
        { first: "Clark", last: "Yoon" },
        { first: "Michelle", last: "Kim" },
      ],
    };
  },
};
</script>

<style></style>
