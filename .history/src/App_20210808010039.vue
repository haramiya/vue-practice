<template>
  <div>
    <LikeHeader header-text="ヘッダーテキスト">
      <template v-slot:title>
        <h1>こんにちは</h1>
      </template>
      <template v-slot:number>
        <div>
          <h2>トータルのいいね数</h2>
          <p>{{number}}</p>
        </div>
      </template>
    </LikeHeader>
    <LikeNumber :total-number="number" @my-click="number=$event"></LikeNumber>
    <LikeNumber :total-number="number"></LikeNumber>
    <button>Home</button>
    <button>About</button>
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
