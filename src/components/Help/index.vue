<template>
  <div>
    <ul class="help-list">
      <li v-for="command in helpList" :key="helpList[command]">
        <span>{{ command.name }}</span> : {{ command.desc }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "YHelp",
  data() {
    return {
      helpList: [
        { name: "/help", desc: "To see The list of Commands" },
        { name: "/skills", desc: "To see list of my Skills" },
        { name: "/projects", desc: "To see the list of my projects" },
        { name: "/clear", desc: "To clear whatever is on the screen" },
        { name: "/about", desc: "To See Everything about my presonal stuff" },
        { name: "/contact", desc: "To see my information contact" },
      ],
    };
  },
};
</script>

<style scoped>
.help-list {
  list-style: none;
  margin: 5px;
}
.help-list > li {
  padding: 10px;
  font-size: 16px;
}
span {
  color: yellow;
}
</style>
