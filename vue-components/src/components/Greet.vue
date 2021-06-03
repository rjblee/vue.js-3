<template>
  <div>Hi {{ name }} aka {{ heroName }}</div>
</template>

<script>
export default {
  name: "Ralph",
  props: ["name", "heroName"],
};
</script>

<style lang="scss" scoped></style>
