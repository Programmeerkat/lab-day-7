<template>
  <div class="month-container">
    <div class="month-name">
      {{ month }}
    </div>
    <div class="month-weeks">
      <v-btn class="month-day">week 1</v-btn>
      <v-btn class="month-day">week 2</v-btn>
      <v-btn class="month-day">week 3</v-btn>
      <v-btn class="month-day">week 4</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: "DayComponent",
  props: {
    month: String,
  },
};
</script>

<style scoped>
.month-container {
  background-color: #f1f1f1;
  width: 100px;
  padding: 10px;
  text-align: center;
  vertical-align: middle;
  font-size: 30px;
  border-radius: 5px;
  margin: 10px;
  box-shadow: 5px 5px 5px gray;
  display: flex;
  flex-direction: column;
}
.month-name {
  padding-bottom: 10px;
}
.month-weeks {
  display: flex;
  flex-direction: column;
  font-size: 10px;
}
</style>
