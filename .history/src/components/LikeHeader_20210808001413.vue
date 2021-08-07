<template>
  <div>
    <slot name="title">
      <h2>デフォルトのタイトル</h2>
    </slot>
    <slot name="number"></slot>
    <p>{{headerText}}</p>
  </div>
</template>

<script>
export default {
  props: ["headerText"]
}
</script>

<style scoped>
div {
  border: 1px solid yellow;
}
</style>