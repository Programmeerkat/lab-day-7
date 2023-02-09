<template>
  <div class="month-container">
 {{ month }}
  </div>
</template>

<script>
export default {
  name: 'DayComponent',
  props: {
    month: String
  }
}
</script>

<style scoped>
.month-container {
  background-color: #f1f1f1;
  width: 100px;
  height: 100px;
  padding: 10px;
  text-align: center;
  vertical-align: middle;
  font-size: 30px;
  border-radius: 5px;
  margin: 10px;
  box-shadow: 5px 5px 5px gray;
}
</style>
