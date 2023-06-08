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
          name: "Anil Group",
          desc: "Architechture Website",
          link: "http://www.anilgroup.co/",
        },
        {
          name: "Morent",
          desc: "A Platform to Rent Cars fast and Easyly",
          link: "https://morent1.netlify.app/",
        },
        {
          name: "Quote App",
          desc: "Using An api to display quotes",
          link: "https://vuequote.netlify.app/",
        },
        {
          name: "DigiZone",
          desc: "An Online Shop",
          link: "https://digizone.netlify.app/",
        },
        {
          name: "Password-Generator",
          desc: "Generate Strong Password And Save them ",
          link: "https://passgenvue.netlify.app",
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
          name: "Calculator",
          desc: "NeedLess",
          link: "https://mycalculatorvue.netlify.app/",
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
