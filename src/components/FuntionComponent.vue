<template>
  <div>
    <button @click="onBtnClick">Click me</button>
  </div>
</template>
<script>
export default {
  props: {
    onBtnClick: {
      type: Function,
      requried: true,
    },
  },
};
</script>
