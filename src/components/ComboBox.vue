<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12">
        <v-combobox v-model="select" :items="items" label="Select task" multiple chips></v-combobox>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: {
    tasks: Array
  },
  data() {
    return {
      select: [],
      items: this.tasks
    };
  }
};
</script>
