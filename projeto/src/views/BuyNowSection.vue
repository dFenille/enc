<template>
  <div id="buy-now" class="bg-blue-img">
    <div class="title-container pt-5">
      <h1 class="title m-0">Compre agora e participe</h1>
    </div>

    <div class="d-flex justify-content-center py-5">
      <div class="d-flex flex-column align-items-center mx-4">
        <img src="../assets/buy-now/pda.png" alt="" />
        <MainButton text="GPA" class="mt-4 main-button" />
      </div>

      <div class="d-flex flex-column align-items-center mx-4">
        <img src="../assets/buy-now/carrefour.png" alt="" />
        <MainButton text="Carrefour" class="mt-4 main-button" />
      </div>
    </div>
  </div>
</template>

<script>
import MainButton from "@/components/MainButton.vue";

export default {
  name: "BuyNowSetion",

  components: {
    MainButton,
  },
};
</script>

<style scoped>
#buy-now {
  font-family: "BrandonGrotesqueBlack", sans-serif;
  text-transform: uppercase;
}

.title-container {
  border-bottom: 3px solid white;
  display: inline-block;
}

.title {
  font-family: "TrendSansFive", sans-serif;
  text-transform: uppercase;
  color: white;
  font-size: 42px;
}

.main-button {
  height: 40px;
  width: 160px;
  font-size: 20px;
}

@media screen and (max-width: 768px) {
  .title-container {
    width: 80%;
  }
}
</style>
