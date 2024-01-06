<template>
  <div id="how-to-participate" class="container-fluid p-0">
    <div class="bg-blue-solid card-container">
      <div class="title-container">
        <h1 class="title m-0">Como participar</h1>
      </div>

      <div class="row steps-container">
        <div class="col-12 col-sm-6 col-xl-3 p-2" v-for="n in 4" :key="n">
          <img
            :src="require(`../assets/how-to-participate/passo-${n}.png`)"
            alt=""
          />
        </div>
      </div>

      <div class="row px-5">
        <div
          class="col-12 col-sm-6 col-xl-3"
          :class="n === 4 && 'col-12'"
          v-for="n in 4"
          :key="n"
        >
          <img
            :src="require(`../assets/how-to-participate/extra-${n}.png`)"
            alt=""
            class="p-2 w-100"
          />
        </div>
      </div>

      <div class="button-container">
        <MainButton text="Participe" class="main-button" />
      </div>
    </div>
  </div>
</template>

<script>
import MainButton from "@/components/MainButton.vue";

export default {
  name: "HowToParticipateSection",

  components: {
    MainButton,
  },
};
</script>

<style scoped>
.card-container {
  padding: 38px 90px;
}

.title-container {
  border-bottom: 3px solid white;
  display: inline-block;
}

.title {
  font-family: "TrendSansFive", sans-serif;
  text-transform: uppercase;
  color: white;
}

.steps-container {
  padding: 48px 48px 0;
}

.button-container {
  padding: 32px;
}

.main-button {
  font-size: 42px;
  padding: 14px 42px;
}

@media screen and (max-width: 768px) {
  .card-container {
    padding: 38px 20px;
  }

  .steps-container {
    padding: 24px 48px 0;
  }

  .button-container {
    padding: 24px;
  }

  .main-button {
    font-size: 2rem;
    padding: 0.8rem 2rem;
  }
}
</style>
