<template>
  <div class="week-container">
    <DayComponent day="Mon" date="01-01-2023" hours="0"/>
    <DayComponent day="Mon" date="01-01-2023" hours="0"/>
    <DayComponent day="Mon" date="01-01-2023" hours="0"/>
    <DayComponent day="Mon" date="01-01-2023" hours="0"/>
    <DayComponent day="Mon" date="01-01-2023" hours="0"/>
    <DayComponent day="Mon" date="01-01-2023" hours="0"/>
    <DayComponent day="Mon" date="01-01-2023" hours="1"/>
  </div>
</template>

<script>
import DayComponent from './DayComponent.vue'

export default {
  name: 'WeekComponent',
  components: {
    DayComponent,
},
  props: {
    msg: String,
    day: String,
    hours: String
  }
}
</script>

<style scoped>
.week-container {
  display: flex;
  flex-wrap: nowrap;
  background-color: DodgerBlue;
}
</style>
