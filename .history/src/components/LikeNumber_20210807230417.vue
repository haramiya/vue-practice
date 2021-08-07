<template>
  <div>
    <p>いいね（{{ number /2 }}）</p>
    <button @click="increment">+1</button>
  </div>
</template>

<script>
export default {
  props: {
    totalNumber: {
      type: Number,
      // required: true,
      default: 5
    }
  },
  methods: {
    incriment() {
      this.number += 1;
    }
  }
}
</script>

<style scoped>
div {
  border: 1px solid red;
}
</style>
