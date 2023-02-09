<template>
<img alt="Clarify logo" src="./assets/logo.png" height="100" />
<div class="main-container">
    <div class="tab-container">
      <WeekComponent/>
    </div>
    <div class="combobox-container">
      <ComboBox v-bind:tasks="tasks" />
    </div>
  </div>
</template>

<script>
import WeekComponent from "./components/WeekComponent.vue";
import ComboBox from "./components/ComboBox.vue";

export default {
  name: "App",
  components: {
    ComboBox,
    WeekComponent
  },
  data() {
    return {
      tasks: [
        "105781 - Boels",
        "100213 - Vacation",
        "100123 - Doctor",
        "100622 - Dentist",
        "100101 - Availability",
        "100523 - Education"
      ]
    };
  }
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
.main-container {
    display: flex;        
  }
  .combobox-container{
    flex:1;
  }
  .tab-container{
    flex:4;
  }
</style>
