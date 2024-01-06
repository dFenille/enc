<template>
  <div id="prizes" class="container-fluid p-0 bg-blue-img">
    <div class="desktop-container">
      <CardContainer>
        <template v-slot:content>
          <div class="section-card-container">
            <img src="../assets/prizes/premios.png" alt="" class="w-100" />
          </div>
        </template>
      </CardContainer>
    </div>

    <div class="mobile-container">
      <CardContainer>
        <template v-slot:content>
          <div class="section-card-container">
            <img
              src="../assets/prizes/premios-mob.png"
              alt=""
              class="prizes-img"
            />
          </div>
        </template>
      </CardContainer>
    </div>
  </div>
</template>

<script>
import CardContainer from "@/components/CardContainer.vue";

export default {
  name: "PrizesSection",

  components: {
    CardContainer,
  },
};
</script>

<style scoped>
.mobile-container {
  display: none;
}

.section-card-container {
  padding: 38px 148px;
}

@media screen and (max-width: 992px) {
  .desktop-container {
    display: none;
  }

  .mobile-container {
    display: block;
  }

  .prizes-img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }

  .section-card-container {
    padding: 14px;
  }
}
</style>
