<template>
  <div class="event" :style="styleObject">
    <div class="event-name">{{ title }}</div>
    <div class="event-start-time event-time">{{ startTime }}</div>
    <div class="event-end-time event-time">{{ endTime }}</div>
  </div>
</template>

<script>
export default {
  name: "Event",
  props: {
    title: String,
    startTime: String,
    endTime: String,
    height: Number,
  },
  data() {
    return {
      styleObject: {
        height: "100px",
        width: "100%",
      },
    };
  },
};
</script>

<style scoped>
.event {
  background: var(--color-primary);
  border-radius: 10px;
  padding: 10px;
  position: relative;
}

.event-name {
  font-size: var(--font-size-m);
  font-weight: 700;
}

.event-time {
  font-size: var(--font-size-m);
  font-style: italic;
  color: var(--color-grey);
  position: absolute;
  padding: inherit;
}

.event-start-time {
  top: 0;
  right: 0;
}

.event-end-time {
  bottom: 0;
  right: 0;
}
</style>
