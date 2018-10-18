<template>
  <div id="app">
    <h2>Top component sees: {{ field }}</h2>
    <hr />
    <Test :value="field" />
  </div>
</template>

<script>
import Test from "./components/Test";

export default {
  name: "App",
  data: () => ({
    field: {
      x: 1,
      y: "one",
      z: "hello"
    }
  }),
  components: {
    Test
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
