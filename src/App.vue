<template>
  <ComboBox/>
  Example of  a week
  <WeekComponent/>
</template>

<script>
import WeekComponent from './components/WeekComponent.vue'
import ComboBox from "./components/ComboBox.vue";

export default {
  name: 'App',
  components: {
    WeekComponent,
    ComboBox,
  }
}
</script>
