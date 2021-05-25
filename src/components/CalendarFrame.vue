<template>
  <div class="calendar-frame">
    <div class="time-frame" v-for="time in times" v-bind:key="time">
      <span class="time-label">{{ time }}</span>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    times() {
      const _times = [];
      for (let i = 6; i <= 23; i++) {
        _times.push(i.toString().padStart(2, "0") + ":00");
      }
      return _times;
    },
  },
};
</script>

<style scoped>
  .calendar-frame {
    display: flex;
    flex-direction: column;
    height: 1000px;
  }

  .time-frame {
    flex-grow: 1;
  }

  .time-label {
    font-size: var(--font-size-s);
    font-weight: 900;
  }
</style>