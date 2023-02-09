<template>
  <v-container fluid>
    <img alt="Clarify logo" src="./assets/logo.png" height="100" />
    <v-select
      v-model="select"
      :items="weekNumbers"
      :menu-props="{ top: true, offsetY: true }"
      label="Weeknumber"
    ></v-select>
    <ComboBox v-bind:tasks="tasks" />
    Example of a week {{ select }}
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
    ComboBox,
  },
  data: () => ({
    tab: null,
    weekNumbers: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16],
    select: null,
    tasks: [
      "105781 - Boels",
      "100213 - Vacation",
      "100123 - Doctor",
      "100622 - Dentist",
      "100101 - Availability",
      "100523 - Education",
    ],
  }),
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
