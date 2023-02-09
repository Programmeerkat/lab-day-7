<template>
    <v-row>
      <v-col cols="12">
        <v-combobox v-model="select" :items="items" label="Select task" multiple chips></v-combobox>
      </v-col>
    </v-row>
</template>

<script>
export default {
  data() {
    return {
      select: [],
      items: [
        "105781 - Boels",
        "100213 - Vacation",
        "100123 - Doctor",
        "100622 - Dentist",
        "100101 - Availability",
        "100523 - Education"
      ]
    };
  }
};
</script>
