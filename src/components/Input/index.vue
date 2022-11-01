<template>
  <form @submit.prevent="submit()">
    <label>~Pooya >> </label>
    <input
      class="input"
      :id="pid"
      type="text"
      placeholder="Try /help"
      v-model="inputValue"
    />
  </form>
</template>

<script>
export default {
  name: "YInput",
  props: ["pid"],
  data() {
    return {
      inputValue: null,
    };
  },
  methods: {
    submit() {
      this.$emit("SendingInputValue", this.inputValue);
      this.inputValue = "";
    },
  },
};
</script>

<style scoped>
.input {
  background-color: inherit;
  border: none;
  outline: none;
  color: yellow;
  width: 300px;
  height: 50px;
}
label {
  font-size: 16px;
  color: #fff;
  margin-left: 50px;
}
</style>
