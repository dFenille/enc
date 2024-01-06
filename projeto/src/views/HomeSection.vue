<template>
  <div id="home" class="container-fluid">
    <div
      class="desktop-container row justify-content-between bg-blue-img fill-height"
    >
      <div
        class="col-6 p-4 pb-0 fill-height d-flex justify-content-center align-items-end"
      >
        <img src="../assets/home/logo-promo.png" alt="" class="h-100" />
      </div>

      <div class="col-6 row p-4 pb-0 fill-height d-flex flex-column">
        <div class="row logo-container">
          <div class="col-12 d-flex justify-content-end">
            <img
              src="../assets/home/logo-unilever.png"
              alt=""
              class="unilever-logo"
            />
          </div>
        </div>

        <div class="row button-container">
          <div class="col-12 d-flex justify-content-start">
            <MainButton text="Participe" class="main-button" />
          </div>
        </div>

        <div class="row flex-grow products-container">
          <div class="col-12 d-flex justify-content-start align-items-end">
            <img
              src="../assets/home/produtos-home.png"
              alt=""
              class="products-img"
            />
          </div>
        </div>
      </div>
    </div>

    <div class="mobile-container row bg-blue-img">
      <div
        class="col-12 p-4 d-flex flex-column justify-content-center align-items-center"
      >
        <img
          src="../assets/home/logo-promo.png"
          alt=""
          class="logo-promo-img"
        />

        <MainButton text="Participe" class="main-button" />
      </div>
    </div>
  </div>
</template>

<script>
import MainButton from "@/components/MainButton.vue";

export default {
  name: "HomeSection",

  components: {
    MainButton,
  },
};
</script>

<style scoped>
#home {
  margin-top: 64px;
}

.flex-grow {
  flex-grow: 1;
}

.mobile-container {
  display: none;
}

.logo-container {
  padding: 2rem 6rem 0;
}

.unilever-logo {
  max-height: 80px;
}

.button-container {
  padding: 3rem 6rem 0;
}

.main-button {
  font-size: 42px;
  padding: 14px 42px;
}

.products-container {
  position: relative;
}

.products-img {
  height: auto;
  width: 125%;
  object-fit: cover;
  margin-left: -224px;
  max-width: 1128px;
  min-width: 760px;
}

@media screen and (max-width: 1128px) {
  .button-container {
    padding: 3rem 4rem 0;
  }

  .main-button {
    font-size: 32px;
    padding: 14px 42px;
  }
}

@media screen and (max-width: 768px) {
  .desktop-container {
    display: none;
  }

  .mobile-container {
    display: block;
  }

  .logo-promo-img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }

  .logo-container {
    padding: 0;
  }

  .button-container {
    padding: 0;
  }

  .main-button {
    font-size: 2rem;
    padding: 0.8rem 2rem;
  }
}
</style>
