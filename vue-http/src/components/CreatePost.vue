<template>
  <div>
    <form action="">
      <label for="userId">Post Id</label>
      <input type="text" id="userId" />

      <label for="title">Post Title</label>
      <input type="text" id="title" />

      <label for="body">Post Body</label>
      <input type="text" id="body" />

      <button>Sumit</button>
    </form>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: CreatePost,
  data() {
    return {
      formData: {
        userId: "",
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      axios
        .post("https://jsonplaceholder.typicode.com/posts", this.formData)
        .then((response) => console.log(response))
        .catch((error) => console.log(error));
    },
  },
};
</script>

<style scoped></style>
