<template>
  <table>
    <thead>
      <!-- for calculating the date and adding it as table header -->
      <!-- <td>month</td>
      <td v-for="day in days" :key="{ day }">
        {{}}
        {{ getDate(newDates.indexOf(day.weekNumber)) }}
      </td> -->
    </thead>
    <tbody>
      <tr>
        <td>hours</td>
        <td v-for="(hour, index) in dates.hours" :key="hour.date">
          <input type="number" v-model="newDates.hours[index]" />
        </td>
      </tr>
    </tbody>
    <button @click="logHours()">log Hours</button>
  </table>
</template>

<script>
export default {
  name: "WeekTable",
  props: {
    dates: Array,
  },
  data() {
    return {
      newDates: this.dates,
      days: [1, 2, 3, 4, 5, 6, 7],
    };
  },

  methods: {
    getMonth: function () {
      let date = new Date();
      return new Intl.DateTimeFormat("en-EN", { month: "long" }).format(date);
    },
    getDay: function (offset) {
      let date = new Date();
      date.setDate(date.getDate() + offset);
      return new Intl.DateTimeFormat("en-EN", { weekday: "long" }).format(date);
    },
    getDate: function (offset) {
      let date = new Date();
      let day = date.getDate() + offset;
      let month = date.getMonth() + 1;
      return `${day}-${month}`;
    },
    logHours: function () {
      console.log(this.newDates);
    },
  },
};
</script>

<style></style>
