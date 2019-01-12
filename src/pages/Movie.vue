<template>
  <div>
    <MovieTemplate :items="items"></MovieTemplate>
  </div>
</template>

<script>
import MovieTemplate from "../components/movie/MovieTemplate";
export default {
  data() {
    return {
      items: []
    };
  },
  methods: {},
  components: {
    MovieTemplate
  },
  computed: {},
  beforeCreate() {
    // /api/someApi
    this.axios.get("/api/someApi").then(res => {
      this.items = res.data.movie;
      console.log(res.data)
    });
  }
};
</script>

<style scoped>
</style>
