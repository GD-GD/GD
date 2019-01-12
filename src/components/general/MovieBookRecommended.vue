<template>
  <div id="movie-child">
    <el-row>
      <el-col class="l-flex">
        <div class="item" v-for="(v,i) in datainfo">
          <el-row class="img">
            <img :src="v.images.medium" alt>
          </el-row>
          <el-row>
            <p class="title">{{v.title}}</p>
          </el-row>
          <el-row class="ll">
            <el-rate
              v-model="v.rating.average"
              disabled
              show-score
              text-color="#ff9900"
              score-template="{value}"
            ></el-rate>
          </el-row>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text:""
    };
  },
  methods: {},
  props: ["datainfo"]
};
</script>

<style scoped>
img {
  width: 100px;
  height: 142px;
  margin: 20px 10px 0 0;
}
.title {
  text-align: center;
  font-size: 15px;
}
.l-flex {
  display: flex;
}
.ll {
  padding: 10px;
}
i {
  font-size: 12px;
}
</style>
