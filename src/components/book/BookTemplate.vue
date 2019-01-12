<template>
  <div class="book">
    <HeadNavBar></HeadNavBar>
    <Parent title_text="最受关注图书|虚构类" :dataitems="datainfo.slice(0,8)"></Parent>
    <Parent title_text="最受关注图书|非虚构类" :dataitems="datainfo.slice(8,16)"></Parent>
  </div>
</template>

<script>
import HeadNavBar from "../general/HeadNavBar";
import Child from "../general/MovieBookRecommended";
import Parent from "../general/MovieBookRecommendParent";

export default {
  data() {
    return {};
  },
  methods: {},
  components: {
    HeadNavBar,
    Child,
    Parent
  },
  props: ["datainfo"]
};
</script>

<style>
</style>
