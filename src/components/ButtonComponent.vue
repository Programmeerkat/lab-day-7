<template>
<button>{{ label }}</button>
</template>

<script>
	export default {
		name: "ButtonComponent",
		props: {
      label: String,
    }
  }
</script>

<style scoped>
button {
  color: white;
  background-color: DodgerBlue;
  border-radius: 5px;
  box-shadow: 5px 5px 5px gray;
  padding: 10px;
  margin: 20px;
}
button:hover {
  background-color: rgb(27, 93, 158);
}
button:active {
  background-color: rgb(27, 93, 158);
  box-shadow: 2px 2px 5px gray;
  transform: translate(3px,3px);
}
</style>