<template>
  <div id="app">
    <div id="box">
      <div>
        <router-view/>
      </div>
    </div>
    <div id="spig" class="spig">
        <div id="message">正在加载中……</div>
        <div id="mumu" class="mumu"></div>
    </div>
  </div>
</template>

<script>
import Canvas from './utils/canvas-nest.js'
import './assets/js/Jq.js'
import './assets/js/spjg.js'
import './assets/css/spigPet.css'
export default {
  components: {
    Canvas
  }
}
</script>
<style lang="scss">
html,body{
  width: 100%;
  height: 100%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: 100%;
  background-image: url('./assets/img/timg (1).jpg');
  background-repeat:no-repeat;
  background-size: 100% 100%;
}
#box{
  width: 1200px;
  height: 100%;
  z-index: 3;
  margin-left: calc((100% - 1200px)/2);
  background: rgba($color: #000000, $alpha: .3);
}
#app{
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
