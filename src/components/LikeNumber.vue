<template>
  <div>
    <p>いいね（{{ number }}）</p>
    <button @click="increment">+1</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 5
    };
  }
}
</script>

<style>
</style>
