<template>
  <TodoItem title="Anki" />
  <Title text="Daily Dashboard" />
  <DateTime text="Montag, 24. Mai 2021" />
  <CalendarFrame />
  <Event
    title="ASE"
    startTime="08:00"
    endTime="12:00"
    v-bind:height="100"
    style="width: 200px"
  />
</template>

<script>
import Title from "./components/Title.vue";
import DateTime from "./components/DateTime.vue";
import CalendarFrame from "./components/CalendarFrame.vue";
import Event from "./components/Event.vue";
import TodoItem from "./components/TodoItem.vue";

export default {
  name: "App",
  components: {
    Title,
    DateTime,
    CalendarFrame,
    Event,
    TodoItem,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap");

:root {
  --color-primary: #ff9292;
  --color-lighter-grey: #c6c6c6;
  --color-light-grey: #878787;
  --color-grey: #454545;
  --font-size-xl: 36px;
  --font-size-l: 24px;
  --font-size-m: 18px;
  --font-size-s: 14px;
  --font-size-xs: 12px;
  --padding: 10px;
  --border-radius: 10px;
}

#app {
  font-family: "Roboto", sans-serif;
}

body {
  margin: 0;
}

h1 {
  margin: 0;
}
</style>
