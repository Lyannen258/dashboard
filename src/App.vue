<template>
  <Title text="Daily Dashboard" />
</template>

<script>
import Title from "./components/Title.vue";

export default {
  name: "App",
  components: {
    Title,
  },
};
</script>

<style>
:root {
  --color-primary: #FF9292;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;

}

body {
  margin: 0;
}

h1 {
  margin: 0;
}
</style>
