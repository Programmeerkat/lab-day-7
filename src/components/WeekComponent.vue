<template>
  <div class="week-container">
    <DayComponent
      v-for="item in weekdata"
      :key="item.date"
      :day="item.day"
      :date="item.date"
      :hours="item.hours"
      :task="item.task"
    />
  </div>
</template>

<script>
import DayComponent from "./DayComponent.vue";

export default {
  name: "WeekComponent",
  components: {
    DayComponent,
  },
  props: {
    weekdata: Array,
  },
};
</script>

<style scoped>
.week-container {
  display: flex;
  justify-content: space-between;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
  background-color: DodgerBlue;
  border-radius: 5px;
  box-shadow: 5px 5px 5px gray;
}
</style>
