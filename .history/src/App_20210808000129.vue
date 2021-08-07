<template>
  <div>
    <LikeHeader>
      <h1>トータルのいいね数</h1>
      <p>{{number}}</p>
    </LikeHeader>
    <LikeNumber :total-number="number" @my-click="number=$event"></LikeNumber>
    <LikeNumber :total-number="number"></LikeNumber>
  </div>
</template>

<script>
import LikeHeader from "./components/LikeHeader.vue"

export default {
  data() {
    return {
      number: 14
    };
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
