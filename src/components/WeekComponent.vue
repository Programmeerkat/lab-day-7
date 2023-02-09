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
  width: 500px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
  background-color: DodgerBlue;
  border-radius: 5px;
  box-shadow: 5px 5px 5px gray;
}
</style>
