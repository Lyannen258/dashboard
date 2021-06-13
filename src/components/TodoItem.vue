<template>
  <div
    class="todo-item"
    :class="{ done: done }"
    v-on:click="toggleDone()"
    v-on:dblclick="preventTextHighlight()"
  >
    <div class="checkbox">
      <div class="checkmark"></div>
    </div>
    <div class="title">{{ title }}</div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
  },
  data() {
    return {
      done: false,
    };
  },
  methods: {
    toggleDone() {
      this.$data.done = !this.$data.done;
    },
    preventTextHighlight() {
      window.getSelection().removeAllRanges();
    },
  },
};
</script>

<style scoped>
.todo-item {
  background: var(--color-primary);
  padding: var(--padding);
  border-radius: var(--border-radius);
  display: flex;
  align-items: center;
}

.done {
  background: var(--color-lighter-grey);
}

.checkbox {
  background: white;
  height: 45px;
  width: 45px;
  border-radius: var(--border-radius);
  margin-right: var(--padding);
  display: flex;
  justify-content: center;
  align-items: center;
}

.checkmark {
  height: 60%;
  width: 60%;
  background: var(--color-grey);
  border-radius: calc(var(--border-radius) / 2);
  display: none;
}

.done .checkmark {
  display: block;
}

.title {
  font-size: var(--font-size-l);
  font-weight: 700;
}

.done .title {
  color: var(--color-light-grey);
  font-style: italic;
}
</style>
