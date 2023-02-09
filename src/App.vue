<template>
  <ComboBox />
  <HelloWorld />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import ComboBox from "./components/ComboBox.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    ComboBox,
  },
};
</script>
