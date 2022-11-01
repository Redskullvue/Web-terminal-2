<template>
  <y-container />
</template>

<script>
import YContainer from "./components/Container/index.vue";

export default {
  name: "App",
  components: {
    YContainer,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: monospace;
}
body {
  background-color: rgb(41, 5, 74);
}
</style>
