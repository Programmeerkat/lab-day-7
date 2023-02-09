<template>
  <v-row>
    <v-col cols="12">
      <v-combobox
        v-model="select"
        :items="items"
        label="Select task"
        multiple
        chips
        @change="emitToParent($event)"></v-combobox>
    </v-col>
  </v-row>
</template>

<script>
import { toRaw } from "vue";

export default {
  props: {
    tasks: Array
  },
  data() {
    return {
      select: [],
      items: this.tasks
    };
  },
  watch: {
    select: function (newValue) {
      this.$emit("childToParent", toRaw(newValue));
    }
  }
};
</script>
