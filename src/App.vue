<template>
  <Table />
</template>

<script>
import Table from "./components/table.vue";

export default {
  name: "App",
  components: {
    Table
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');
*{
  padding:0;
  margin:0;
}
html {
  scroll-behavior: smooth;
}
#app {
  font-family: Inter, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #F7F7F4;
  width:100%;
  height:100%;
}
</style>
