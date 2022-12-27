<template>
  <div class="container">
    <div class="head-title">
      <h3>
        Hi ! My name is <span>Pooya Goodarzi</span> and this is my web terminal
        . if you are in search of information about me check out the terminal
        <span class="dot">|</span>
      </h3>
    </div>
    <!-- pid = props id  -->
    <y-input
      v-for="submit in submitCounts"
      :pid="'i' + submit"
      :key="submit"
      class="inputs"
      @sendingInputValue="setEmitedInputValue($event)"
    />
    <div class="responds">
      <y-help v-if="inputComponentValue == '/help'" />
      <y-project v-if="inputComponentValue == '/projects'" />
      <y-skills v-if="inputComponentValue == '/skills'" />
      <y-about v-if="inputComponentValue == '/about'" />
      <y-contact v-if="inputComponentValue == '/contact'" />
      <p v-if="showError">
        {{ inputComponentValue }}
        <span>Is not a command try <span>/help</span> </span>
      </p>
    </div>
  </div>
</template>

<script>
import YInput from "../Input/index.vue";
import YHelp from "../Help/index.vue";
import YSkills from "../skills/index.vue";
import YProject from "../Projects/index.vue";
import YAbout from "../About/index.vue";
import YContact from "../contact/index.vue";

export default {
  name: "YContainer",
  components: {
    YInput,
    YHelp,
    YSkills,
    YProject,
    YAbout,
    YContact,
  },

  data() {
    return {
      inputComponentValue: "",
      submitCounts: [0],
      counter: 1,
      showError: false,
      id: 0,
    };
  },
  //  I used this lifecycle hook for the responsive idea that i have
  mounted() {
    setInterval(() => {
      document.querySelector(".head-title").style =
        "white-space : wrap; overflow :visible ";
    }, 3000);
  },

  methods: {
    setEmitedInputValue(event) {
      this.inputComponentValue = event;
      this.submitCounts.push(this.counter++);
      if (
        event != "/help" &&
        event != "/skills" &&
        event != "/projects" &&
        event != "/clear" &&
        event != "/about" &&
        event != "/contact"
      ) {
        this.showError = true;
        setTimeout(() => {
          this.showError = false;
        }, 3000);
      } else if (event == "/clear") {
        this.showError = false;
        this.inputComponentValue = "";
        this.submitCounts.splice(0, this.submitCounts.length - 1);
        console.log(this.counter - 1);
      }
      let testID = "i" + this.id;
      document.getElementById(testID).setAttribute("placeholder", "");
      document.getElementById(testID).setAttribute("disabled", "");
      this.id++;
      console.log(this.submitCounts);
    },
  },
};
</script>

<style scoped>
.container {
  background-color: rgb(41, 5, 74);
  color: #fff;
  display: flex;
  flex-direction: column;
  height: max-content;
  padding: 80px;
}
.responds {
  margin-left: 100px;
}
.inputs {
  margin-left: 60px;
}
.head-title {
  width: 100%;
  margin: 30px 0px;
  font-weight: 500;
  line-height: 1.9;
  text-align: center;
  animation: typing 3s;
  white-space: nowrap;
  overflow: hidden;
}
span {
  color: yellow;
}
.dot {
  animation: dot 1s infinite;
}
@keyframes dot {
  0% {
    opacity: 100%;
  }
  50% {
    opacity: 0%;
  }
  100% {
    opacity: 100%;
  }
}
@keyframes typing {
  from {
    width: 0%;
  }
  to {
    width: 100%;
  }
}
</style>
