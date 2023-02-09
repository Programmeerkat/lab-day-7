<template>
  <v-container fluid>
    <img alt="Clarify logo" :src="require('./assets/logo.png')" height="100" />
    <v-select v-model="select" :items="getWeeks()" :menu-props="{ top: true, offsetY: true }" label="Week"></v-select>
    <ComboBox v-bind:tasks="tasks" weekNumber="" v-on:childToParent="onChildClick" />
    Example of a week {{ select }}
    <ButtonComponent label="Add task" />
    <Periods :week="select" />
  </v-container>
</template>

<script>
import Periods from "./components/Periods.vue";
import ComboBox from "./components/ComboBox.vue";
import ButtonComponent from "./components/ButtonComponent.vue";

export default {
  name: "App",
  components: {
    Periods,
    ComboBox,
    ButtonComponent
  },
  data: () => ({
    tab: null,
    select: null,
    tasks: [
      "105781 - Boels",
      "100213 - Vacation",
      "100123 - Doctor",
      "100622 - Dentist",
      "100101 - Availability",
      "100523 - Education"
    ],
    selectedTasks: []
  }),
  methods: {
    getWeeks() {
      const weeks = [
        "1/1 - 7/1",
        "8/1 - 14/1",
        "15/1 - 21/1",
        "22/1 - 28/1",
        "29/1 - 31/1",
        "1/2 - 7/2",
        "8/2 - 14/2",
        "15/2 - 21/2",
        "22/2 - 28/2"
      ];
      return weeks;
    },
    // Triggered when `childToParent` event is emitted by the child.
    onChildClick(value) {
      this.selectedTasks = value;
    }
  }
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
