<template>
  <div class="hello">
    <h1>Clarity</h1>
    <div class="container">
      <button
        @click="
          {
            this.weeksView = !this.weeksView;
          }
        "
      >
        weeks
      </button>
      <button
        @click="
          {
            this.monthsView = !this.monthsView;
          }
        "
      >
        month
      </button>
      <button
        @click="
          {
            this.quartersView = !this.quartersView;
          }
        "
      >
        quarter
      </button>

      <select id="weeks" name="weeks">
        <option v-for="week in weeks" :key="week">
          {{ week }}
        </option>
      </select>

      <div v-if="weeksView">
        <WeekTable :dates="dates[0]"></WeekTable>
      </div>

      <button>add task</button>
    </div>
  </div>
</template>

<script>
import WeekTable from "./WeekTable.vue";

export default {
  name: "HelloWorld",
  data() {
    return {
      weeks: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12],
      dates: [
        {
          weekNumber: 1,
          hours: [8, 8, 8, 8, 8, 8, 8],
          date: new Date(),
          projectCode: "x",
        },
        {
          weekNumber: 2,
          hours: [8, 8, 8, 8, 8, 8, 8],
          date: new Date(),
          projectCode: "y",
        },
      ],
      weeksView: true,
      monthsView: false,
      quartersView: false,
    };
  },
  props: {},
  components: {
    WeekTable,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
