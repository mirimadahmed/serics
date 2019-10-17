<template>
  <div id="app">
    <MainHeader />
  </div>
</template>

<script>
import MainHeader from "@/components/MainHeader.vue";

export default {
  name: "app",
  components: {
    MainHeader
  }
};
</script>

<style>
body {
  margin: 0px;
  color: white;
  background: #54a0ff;
  width: 100%;
  height: 100vh;
  text-align: center;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#app {
  height: 100%;
}
</style>
