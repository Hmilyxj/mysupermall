<template>
  <div class="recommend" @click="godetail">
    <div v-for="item in recommends" class="recommend-item">
      <!-- <a :href="item.link"> -->
        <a>
        <img v-lazy="item.image" alt="" :key="item.image">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name:"HomeRecommendView",
  props: {
    recommends:{
      type:Array,
      default(){
        return [];
      },
    }
  },
  methods: {
    godetail(){
      this.$router.push('/details/1m70y5k');
    }
  }
}
</script>

<style scoped>
.recommend{
  display:flex;
  width:100%;
  text-align:center;
  font-size:12px;
  padding:10px 0 20px 0;
  border-bottom: 10px solid #eee;
}
.recommend-item{
  flex:1;
  width:20%;
  height:20%;

}
.recommend-item img{
 width:80%;
 margin-bottom: 10px;
}
</style>