<template>
  <div>
    <button @click="getPosts">Load Posts</button>
    <div v-for="post in posts" :key="post.id">
      <h3>{{ post.id }}</h3>
      <h4>{{ post.title }}</h4>
      <p>{{ post.body }}</p>
      <hr />
    </div>
    <div v-if="errorMessage">{{ errorMessage }}</div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "PostList",
  data() {
    return {
      posts: [],
      errorMessage: "",
    };
  },
  methods: {
    getPosts() {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((response) => {
          console.log(response.data);
          this.posts = response.data;
        })
        .catch((error) => {
          console.log(error);
          this.errorMessage = "Error during fetching";
        });
    },
  },
};
</script>

<style scoped></style>
