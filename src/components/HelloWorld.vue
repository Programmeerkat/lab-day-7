<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <v-container fluid>
        <ComboBox />
        <Periods />
    </v-container>
  </div>
</template>

<script>
import ComboBox from "./ComboBox.vue";
import Periods from "./Periods.vue";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    ComboBox,
    Periods
  }
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
