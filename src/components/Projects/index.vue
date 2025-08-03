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
          name: "Daravin",
          desc: "An automatic e-commerce builder + marketplace (Launch : 10/8/2025) - my biggest project ever - Back-end and Front-end Developed by myself",
          link: "https://daravin.ir",
        },
        {
          name: "Anil Group",
          desc: "Architechture Website (There Are Some Copies in the code)",
          link: "http://www.anilgroup.co/",
        },
        {
          name: "Morent",
          desc: "A Platform to Rent Cars fast and Easyly (UI Developed)",
          link: "https://morent1.netlify.app/",
        },
        {
          name: "Webeez Website",
          desc: "Software Company - a personal project introducing me and my work (Dev mode)",
          link: "https://webeez1.netlify.app/",
        },
        {
          name: "Dodge Cube",
          desc: "Dont Let the cubes hit u ;  a 3D game using three js ",
          link: "https://dodgecube.netlify.app/",
        },
        {
          name: "O'studio",
          desc: "Architecture Group Website",
          link: "http://ostudio.design/",
        },

        {
          name: "DigiZone",
          desc: "An Online Shop (Test)",
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
          desc: "Pure HTML and CSS Layout of a resturant website ",
          link: "https://deliciousfoodlayout.netlify.app/",
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
