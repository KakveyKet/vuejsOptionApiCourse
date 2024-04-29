<template>
  <div class="hello">
    <h1 :style="{ color: color, fontWeight: fontWeight }">Hello Guy</h1>
    <div v-for="(item, index) in myList" :key="index">
      <div>
        <button @click="myData(item.name)">Click</button>
        <button @click="myDataRemove(index)">Remove</button>
      </div>
      <h1 :class="[a, b]">this is the {{ item.name }} with {{ item.id }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        name: "hello",
      },
      arr: [],
      className: "color-blue",
      isActive: true,
      a: "A",
      b: "B",
      color: "purple",
      fontWeight: "800",
      myList: [
        {
          id: 1,
          name: "test0",
          isActive: true,
        },
        {
          id: 2,
          name: "test1",
          isActive: false,
        },
        {
          id: 3,
          name: "test2",
          isActive: true,
        },
      ],
    };
  },
  methods: {
    myData(data) {
      console.log("====================================");
      console.log(data);
      console.log("====================================");
    },
    myDataRemove(index) {
      this.myList.splice(index, 1);
    },
  },
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.color-red {
  color: red;
}
.color-blue {
  color: blue;
}
.active {
  color: green;
}
.back {
  background-color: aqua;
}
.A {
  color: red;
  margin: 5px;
  padding: 20px;
}
.B {
  background-color: aqua;
}
</style>
