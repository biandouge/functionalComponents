<template>
<div id="app">
  <button @click="normalCount = 10000">生成10000个普通组件</button>
  <button @click="functionalCount = 10000">生成10000个函数组件</button>
  <div class="container">
    <div class="item">
      <NormalComp v-for="n in normalCount" :key="n" :count="n"></NormalComp>
    </div>

    <div class="item">
      <FunctionalComp
      v-for="n in functionalCount"
      :key="n"
      :count="n"
      ></FunctionalComp>
    </div>
  </div>
</div>
</template>

<script>
import NormalComp from "./components/NormalComp.vue";
import FunctionalComp from "./components/FunctionalComp.vue";

export default {
  name: 'App',
  components: {
    NormalComp,
    FunctionalComp,
  },
  data(){
    return{
      functionalCount: 0,
      normalCount: 0,
    }
  },
  mounted(){
    window.vm = this;
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container{
  display: flex;
  justify-content: center;

}
</style>
