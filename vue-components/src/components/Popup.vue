<template>
  <div>
    <h2>This is a popup</h2>
    <button @click="$emit('close')">Close</button>
  </div>
</template>

<script>
export default {
  name: "Popup",
  emits: ["close"],
};
</script>

<style lang="scss" scoped></style>
