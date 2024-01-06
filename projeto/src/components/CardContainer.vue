<template>
  <div class="bg-blue-dark-solid main-card-container w-100">
    <div
      class="card-container w-100 d-flex justify-content-center align-items-center"
    >
      <slot name="content" />
    </div>
  </div>
</template>

<script>
export default {
  name: "CardContainer",
};
</script>

<style scoped>
.main-card-container {
  border-radius: 64px;
  padding: 14px;
}

.card-container {
  border-radius: 64px;
  border: 6px solid var(--primary-color);
  /* padding: 38px 148px; */
}
</style>