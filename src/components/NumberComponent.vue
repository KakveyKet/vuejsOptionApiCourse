<template>
  <div>
    {{ totalNumber * 2 }}
  </div>
</template>

<script>
export default {
  props: {
    totalNumber: {
      type: Number,
      default: 100,
    },
  },
  data() {
    return {};
  },
};
</script>
