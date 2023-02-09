<template>
  <v-container fluid>
    <img alt="Clarify logo" :src="require('./assets/logo.png')" height="100" />
    <ComboBox v-bind:tasks="tasks" />
    <p>Example of a week</p>
    <Periods />
  </v-container>
</template>

<script>
import Periods from "./components/Periods.vue";
import ComboBox from "./components/ComboBox.vue";

export default {
  name: "App",
  components: {
    Periods,
    ComboBox
  },
  data: () => ({
    tab: null,
    tasks: [
      "105781 - Boels",
      "100213 - Vacation",
      "100123 - Doctor",
      "100622 - Dentist",
      "100101 - Availability",
      "100523 - Education"
    ]
  })
};
</script>

<style>
#app {
  font-family: Calibri, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
