<template>
  <div>
    <h3>Programming Language : <span>JavaScript</span></h3>
    <h3>
      FrameWorks and Libraries :
      <span v-for="frameWork in frameworks" :key="frameWork"
        >{{ frameWork }}-</span
      >
    </h3>
    <h3>
      Dev Tools : <span v-for="tool in devTools" :key="tool">{{ tool }}-</span>
    </h3>
    <h3>
      Os : <span v-for="os in opreatingSystem" :key="os">{{ os }}-</span>
    </h3>
  </div>
</template>

<script>
export default {
  name: "YSkills",
  data() {
    return {
      frameworks: [
        "Vuejs",
        "Nuxt Js",
        "TailwindCSS",
        "Axios",
        "WebPack",
        "Vue Router",
        "Vuex",
        "VueCli",
      ],
      devTools: ["Visual Studio Code", "Git", "Npm", "Yarn"],
      opreatingSystem: ["Windows", "Ubuntu"],
    };
  },
};
</script>

<style scoped>
h3 {
  color: yellow;
}
h3 > span {
  color: #fff;
}
</style>
