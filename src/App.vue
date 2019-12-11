<template>
  <div id="app">
    <Popover>
      <template v-slot:content>
        <div>
          <h1>我是popover</h1>
        </div>
      </template>
      <button>点我弹出popover</button>
    </Popover>
  </div>
</template>

<script>
import Popover from "./components/popover";

export default {
  name: "App",
  components: {
    Popover
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  padding: 100px;
}
</style>
