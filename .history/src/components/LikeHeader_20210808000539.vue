<template>
  <div>
    <slot></slot>
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