<template>
  <div>
    <h3>Here Are some of the Projects i have done through out the timne :</h3>
    <ul>
      <li v-for="project in projects" :key="project.name">
        <a :href="project.link">{{ project.name }}</a> : {{ project.desc }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "YProject",
  data() {
    return {
      projects: [
        {
          name: "SplusTuning-Recipt",
          desc: "Printing Out Factors ",
          link: "https://splustest.netlify.app/",
        },
        {
          name: "Weather-App",
          desc: "Showing The Weather Using API",
          link: "https://myvueweatherapp1.netlify.app/",
        },
        {
          name: "Delicous-Food",
          desc: "Pure HTML and CSS Layout of a resturant ",
          link: "https://deliciousfoodlayout.netlify.app/",
        },
        {
          name: "Callculator",
          desc: "NeedLess",
          link: "https://mycalculatorvue.netlify.app/",
        },
        {
          name: "ToDo-App",
          desc: "TaskManager",
          link: "https://todovue1.netlify.app/",
        },
        {
          name: "Password-Generator",
          desc: "Generate Strong Password And Save them ",
          link: "#",
        },
      ],
    };
  },
};
</script>

<style scoped>
li {
  list-style: none;
  font-size: 16px;
}
a {
  color: yellow;
}
</style>
