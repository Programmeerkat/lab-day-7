<template>
  <HelloWorld />
  <ComboBox/>
  Example of  a week
  <WeekComponent/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import WeekComponent from './components/WeekComponent.vue'
import ComboBox from "./components/ComboBox.vue";

export default {
  name: 'App',
  components: {
    HelloWorld,
    WeekComponent,
    ComboBox,

  },
  data: () => ({
      tab: null,
    }),
}
</script>
