<template>
  <div class="sayHello">
    <div class="header">
      <slot name="HelloHeader"> </slot>
    </div>
    <div class="body">
      <slot></slot>
    </div>
    <div class="footer">
      <slot name="HelloFooter"> Footer </slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ["data", "data2"],
};
</script>
<style scoped>
.sayHello {
  padding: 20px;
  border: 1px solid red;
  margin-top: 300px;
}
.body {
  background-color: blueviolet;
}
.header {
  background-color: aqua;
}
.footer {
  background-color: blue;
  color: aliceblue;
}
</style>
