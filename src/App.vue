<template>
  <v-container fluid>
    <ComboBox/>
    Example of  a week
    <Periods />
  </v-container>
</template>

<script>
import Periods from './components/Periods.vue'
import ComboBox from "./components/ComboBox.vue";

export default {
  name: 'App',
  components: {
    Periods,
    ComboBox,

  },
  data: () => ({
      tab: null,
    }),
}
</script>
