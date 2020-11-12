<!--
 * @Description: 
 * @version: 
 * @Author: xuml31350
 * @Date: 2020-09-24 09:37:14
 * @LastEditors: xuml31350
 * @LastEditTime: 2020-09-24 14:00:52
-->
<template>
  <img ref="root" alt="Vue logo" src="./assets/logo.png">
  <div v-for="item in [{a:'test1'},{a:'test2'}]" :key="item" :ref="item.a">11</div>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import {ref, onMounted} from 'vue';
export default {
  name: 'App',
  setup() {
    const test1 = ref(null);
    onMounted(() => {
      console.log(test1.value)
    })
    return {test1}
  },
  components: {
    HelloWorld
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
</style>
