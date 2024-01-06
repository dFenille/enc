<template>
  <button>
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "MainButton",

  props: {
    text: { type: String, required: true },
  },
};
</script>

<style scoped>
button {
  background-color: var(--secondary-color);
  font-family: "BrandonGrotesqueBlack", sans-serif;
  color: var(--primary-color);
  text-transform: uppercase;
  border: none;
  box-shadow: 10px 10px 16px -6px rgba(0, 0, 0, 0.6);
  border-radius: 56px;
}
</style>