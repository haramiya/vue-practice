<template>
  <div>
    <slot></slot>
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