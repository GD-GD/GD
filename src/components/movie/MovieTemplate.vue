<template>
  <div id="movie-template">
    <HeadNavBar></HeadNavBar>
    <MovieRecommendParent title_text="影院热映" :dataitems="data1"></MovieRecommendParent>
    <MovieRecommendParent title_text="免费在线观影" :dataitems="data2"></MovieRecommendParent>
    <MovieRecommendParent title_text="新片速递" :dataitems="data3"></MovieRecommendParent>
  </div>
</template>

<script>
import HeadNavBar from "../general/HeadNavBar";
import MovieRecommendParent from "../general/MovieBookRecommendParent";
export default {
  data() {
    return {};
  },
  methods: {},
  components: {
    HeadNavBar,
    MovieRecommendParent
  },
  props: ["items"],
  computed: {
    data1() {
      console.log()
      return this.items.slice(0,8);
    },
    data2() {
      return this.items.slice(8,16);
    },
    data3() {
      return this.items.slice(16,24);
    }
  }
};
</script>

<style scoped>
.ll {
  width: 100px;
}
</style>
