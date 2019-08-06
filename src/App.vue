<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from "./components/layout/Header";

export default {
  name: 'app',
  components: {
    Header
  }
}
</script>


<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
.btn {
  display: inline-block;
  border: 0;
  background-color: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}
</style>
