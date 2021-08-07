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
    <button @click="currentComponent = 'Home'">Home</button>
    <button @click="currentComponent = 'About'">About</button>
    <!-- keep-aliveで動的コンポーネントの中身（テキストボックスなど）をキャッシュする -->
    <keep-alive>
      <component :is="currentComponent"></component>
    </keep-alive>
    <Form></Form>
  </div>
</template>

<script>
import LikeHeader from "./components/LikeHeader.vue"
import About from "./components/About.vue"
import Home from "./components/Home.vue"
import Form from "./components/Form.vue"

export default {
  data() {
    return {
      number: 14,
      currentComponent: "Home"
    };
  },
  components: {
    LikeHeader,
    About,
    Home,
    Form
    // keyとvalueが一緒なので、短縮してLikeHeaderだけでも良い
  }
}
</script>

<style scoped>
div {
  border: 1px solid blue;
}
</style>
