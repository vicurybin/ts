<template>
  <div id='app'>
    <div @click="clicktest">点击测试</div>
    <div >{{computedtest}}</div>
    <img src='./assets/logo.png'>
    <router-view></router-view>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'
@Component({
  // 所有的组件选项都可以放在这里
  props:{
    propmsg:String
  },
  name:'lalal',
  data(){
    return {
      age:'111'
    }
  }
})
export default class App extends Vue {
  msg:number = 133;
  get computedtest (){
    return 'computed'+this.msg;
  }
  clicktest (): void {
      alert('msg'+this.msg)
  }
} 
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
