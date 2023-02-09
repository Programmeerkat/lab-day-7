<template>
  <div class="container">
    <div class="day">{{ day }}</div>
    <div class="date">{{ date }}</div>
    <input type="number" min="0" value="hours">
  </div>
</template>

<script>
export default {
  name: 'DayComponent',
  props: {
    day: String,
    date: String,
    hours: String
  }
}
</script>

<style scoped>
.container {
  background-color: #f1f1f1;
  width: 100px;
  margin: 10px;
  text-align: center;
  line-height: 75px;
  font-size: 30px;
}
.day {
  font-size: 20px;
}
.date {
  font-size: 10px;
}
input {
  background-color: #f1f1f1;
  width: 50px;
  margin: 10px;
  text-align: center;
  line-height: 75px;
  font-size: 30px;
}
</style>
