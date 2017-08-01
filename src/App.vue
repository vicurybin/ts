
<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'
@Component({
  // 所有的组件选项都可以放在这里
  template: "<div id='app'><img src='./assets/logo.png'><router-view></router-view></div>",
  name: 'app'
})
export default class App extends Vue {
  
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
