<template>
  <div>
    <LikeHeader></LikeHeader>
    <p>{{number}}</p>
    <LikeNumber :number="totalNumber" @my-click="number = $event"></LikeNumber>
    <LikeNumber :number="totalNumber"></LikeNumber>
    <LikeTotal></LikeTotal>
  </div>
</template>

<script>
import LikeHeader from "./components/LikeHeader.vue"

export default {
  data() {
    return {
      number: 10
    };
  },
  methods: {
    increment() {
      this.number += 1;
    }
  },
  components: {
    LikeHeader: LikeHeader
    // keyとvalueが一緒なので、短縮してLikeHeaderだけでも良い
  }
}
</script>

<style scoped>
div {
  border: 1px solid blue;
}
</style>
