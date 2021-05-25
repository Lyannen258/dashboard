<template>
  <div>
    <span>
      {{text}}
    </span>
  </div>
</template>

<script>
export default {
  name: "DateTime",
  props: {
    text: String
  },
};
</script>

<style scoped>
  span {
    color: var(--color-light-grey);
    font-size: var(--font-size-l);
    font-style: italic;
  }
</style>