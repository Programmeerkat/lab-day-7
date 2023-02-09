<template>
  <img alt="Clarify logo" src="./assets/logo.png" height="100" />
  <v-container fluid>
    <div class="main-container">
      <div class="tab-container">
        <Periods />
      </div>
      <div class="combobox-container">
        <ComboBox :tasks="tasks" v-on:childToParent="onChildClick" />
      </div>
    </div>
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
    ],
    selectedTasks: []
  }),
  methods: {
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
.main-container {
  display: flex;
}
.combobox-container {
  flex: 1;
}
.tab-container {
  flex: 4;
}
</style>
