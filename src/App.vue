<template>
  <div id='app'>
    <div @click="clicktest">点击测试</div>
    <div>{{propA}}{{propB}}</div>
    <div >{{computedtest}}</div>
    <img src='./assets/logo.png'>
    <router-view></router-view>
  </div>
</template>

<script lang="ts">
// import Vue from 'vue'
// import Component from 'vue-class-component'

import { Component, Inject, Model, Prop,Vue, Watch } from 'vue-property-decorator'
@Component({
  // 所有的组件选项都可以放在这里
  
  name:'lalal',

})
export default class App extends Vue {
  msg:number = 133;
  hello:string = 'hello'
  @Prop({
    default:'lalalala',
  })
  propA:string;

  @Prop()
  propB:any
  
  get computedtest (){
    return 'computed'+this.msg;
  }
  clicktest (): void {
      alert('msg'+this.propA)
  }
  mounted(){
    // alert('mounted'+this.hello)
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
