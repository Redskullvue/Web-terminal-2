<template>
  <div v-for="info in infoes" :key="info.text">
    <h2>
      {{ info.name }} : <a href="info.link"> {{ info.text }}</a>
    </h2>
  </div>
</template>

<script>
export default {
  name: "YContact",
  data() {
    return {
      infoes: [
        { name: "Email", link: "#", text: "pooyaworkjs@gmail.com" },
        { name: "GitHub", link: "#", text: "RedSkullVue" },
      ],
    };
  },
};
</script>

<style></style>
