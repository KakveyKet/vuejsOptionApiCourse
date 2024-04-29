<template>
  <div>
    <h1 v-for="(data, index) in myArr" :key="index">
      {{ data.name }} -- {{ data.age }}
    </h1>
  </div>
</template>
<script>
export default {
  props: {
    myArr: Array,
  },
};
</script>
