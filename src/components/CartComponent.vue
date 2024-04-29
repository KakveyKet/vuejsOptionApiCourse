<template>
  <div class="card">
    <slot name="cardImag"></slot>
    <div class="container">
      <slot></slot>
      <slot name="cartFooter"></slot>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.card {
  width: 400px;
}
.container {
  padding: 2px 16px;
}
</style>
