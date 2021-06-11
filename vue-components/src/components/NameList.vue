<template>
  <h2 v-for="name in names" :key="name.firstName">
    {{ name.firstName }} {{ name.lastName }}
  </h2>
</template>

<script>
export default {
  name: "NameList",
  data() {
    return {
      names: [
        { firstName: "Ralph", lastName: "Lee" },
        { firstName: "Tommy", lastName: "Kim" },
        { firstName: "Andy", lastName: "Seo" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
