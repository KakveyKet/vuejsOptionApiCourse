<template>
  <div :class="`myBox ${isActive ? 'green' : 'red'}`">Boolean Box</div>
</template>

<script>
export default {
  props: {
    isActive: {
      type: Boolean,
      required: true,
      default: true,
    },
  },
  data() {
    return {};
  },
};
</script>
<style scoped>
.myBox {
  width: 200px;
  height: 200px;
}
.red {
  background-color: red;
}
.green {
  background-color: green;
}
</style>
