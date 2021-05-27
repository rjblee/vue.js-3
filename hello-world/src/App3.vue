<template>
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
  <div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>
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
      actors: [
        { name: "Christian Bale", movies: ["Batman", "The Prestige"] },
        { name: "Leonardo DiCaprio", movies: ["Titanic", "Inception"] },
      ],
    };
  },
};
</script>

<style></style>
