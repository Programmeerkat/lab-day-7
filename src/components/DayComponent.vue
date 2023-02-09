<template>
  <div class="container">
    <div class="day">{{ day }}</div>
    <div class="date">{{ date }}</div>
    <input v-bind:value="hours">
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
  margin: 10px;
  text-align: center;
  font-size: 30px;
  border-radius: 5px;
  box-shadow: 5px 5px 5px gray;
  flex-grow: 1;
}
.day {
  font-size: 20px;
  margin: 10px 0 10px 0;
}
.date {
  font-size: 10px;
}
input {
  background-color: #f1f1f1;
  margin: 10px;
  text-align: center;
  font-size: 30px;
  width: 22px;
}
</style>
