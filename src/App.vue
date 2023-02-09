<template>
  <img alt="Clarify logo" src="./assets/logo.png" height="100" />
  <ComboBox v-bind:tasks="tasks" />
  <HelloWorld />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import ComboBox from "./components/ComboBox.vue";

export default {
  name: "App",
  components: {
    ComboBox,
    HelloWorld,
  },
  data() {
    return {
      tasks: [
        "105781 - Boels",
        "100213 - Vacation",
        "100123 - Doctor",
        "100622 - Dentist",
        "100101 - Availability",
        "100523 - Education",
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
