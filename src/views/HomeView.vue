<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <TitleVue :title="page" />
    <button @click="page = 'Hello I am a new page'">
      Click to change value
    </button>
    <UserInforCompoentVue name="Elonton" surname="Jonh" age="35" />
    <BooleanBoxComponentVue :isActive="false" />
    <NumberComponentVue />
    <ObjComponentVue :dog="dog2" />

    <ArrayComponent :myArr="arr" />
    <FunctionComponent :onBtnClick="HandleClick" />
    <Hello>
      <template v-slot:HelloHeader> I'm Header </template>
      <template v-slot:HelloFooter> I'm Footer </template>

      <h1>Hello</h1>
      <p>How are you ?</p>
      <button>Click</button>
      <Test />
    </Hello>
    <br />
    <br />
    <CardComponent>
      <template v-slot:cardImag>
        <img
          style="width: 200px; height: 200px"
          src="https://img.freepik.com/free-vector/hand-drawn-asian-couple-illustration_23-2150043287.jpg?t=st=1714381872~exp=1714385472~hmac=b11f32f5deb6abbbcbf2debc8cdfed06edf4f425bdda1a0c8aa783d009aeff7c&w=996"
          alt="https://img.freepik.com/free-vector/hand-drawn-asian-couple-illustration_23-2150043287.jpg?t=st=1714381872~exp=1714385472~hmac=b11f32f5deb6abbbcbf2debc8cdfed06edf4f425bdda1a0c8aa783d009aeff7c&w=996"
        />
      </template>
      <h1>I'm body</h1>
      <template v-slot:cartFooter>
        <h2>Hi i'm footer</h2>
      </template>
    </CardComponent>
    <div style="height: 100vh">
      <div class="wrapper">
        <button>ComponentA</button><button>ComponentB</button
        ><button>ComponentC</button>
      </div>
      <div style="margin-top: 100px">render</div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import TitleVue from "../components/TitleCompoment.vue";
import UserInforCompoentVue from "../components/UserInforCompoent.vue";
import BooleanBoxComponentVue from "../components/BooleanBoxComponent.vue";

import NumberComponentVue from "../components/NumberComponent.vue";

import ObjComponentVue from "../components/ObjComponent.vue";
import ArrayComponent from "../components/ArrayComponent.vue";
import FunctionComponent from "../components/FuntionComponent.vue";

import Hello from "../components/HelloSlot.vue";
import Test from "../components/TestComponent.vue";
import CardComponent from "../components/CartComponent.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
    TitleVue,
    UserInforCompoentVue,
    BooleanBoxComponentVue,
    NumberComponentVue,
    ObjComponentVue,
    ArrayComponent,
    FunctionComponent,
    Hello,
    Test,
    CardComponent,
  },

  data() {
    return {
      page: "hello I'm a page",
      dog2: {
        name: "hrr",
        gender: "male",
      },
      arr: [
        {
          name: "test",
          age: "20",
        },
        {
          name: "test1",
          age: "21",
        },
      ],
    };
  },
  methods: {
    HandleClick() {
      alert("Hello");
    },
  },
};
</script>
<style scoped>
.wrapper {
  display: flex;
  justify-content: center;
  gap: 10px;
}
button {
  height: 40px;
  display: flex;
  align-items: center;
  border: none;
  border-radius: 10px;
  background-color: #2c3e50;
  color: #fff;
  padding: 20px;
}
</style>
