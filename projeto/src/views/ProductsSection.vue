<template>
  <div id="products" class="bg-blue-solid position-relative">
    <CardContainer>
      <template v-slot:content>
        <div
          class="d-flex flex-column justify-content-start align-items-center section-card-container"
        >
          <div class="title-container">
            <h1 class="title m-0">Produtos participantes</h1>
          </div>

          <h1 class="subtitle pt-3">Todos os squeezes da linha Hellmann's</h1>
        </div>
      </template>
    </CardContainer>

    <div class="pt-5 w-100 position-absolute bottom-0">
      <img class="image" src="../assets/home/produtos-home.png" alt="" />
    </div>

    <img
      class="position-absolute nuggets"
      src="../assets/products/nuggets.png"
      alt=""
    />

    <img
      class="position-absolute chips"
      src="../assets/products/chips.png"
      alt=""
    />
  </div>
</template>

<script>
import CardContainer from "@/components/CardContainer.vue";

export default {
  name: "ProductsSetion",

  components: {
    CardContainer,
  },

  data() {
    return {
      tabs: ["Pratos", "Bowls", "Tábua"],
      selectedTabIndex: 0,
    };
  },
};
</script>

<style scoped>
#products {
  font-family: "BrandonGrotesqueBlack", sans-serif;
  text-transform: uppercase;
}

.section-card-container {
  padding: 38px 64px;
  height: 680px;
}

.title-container {
  border-bottom: 3px solid white;
  display: inline-block;
}

.title {
  font-family: "TrendSansFive", sans-serif;
  text-transform: uppercase;
  color: white;
  font-size: 54px;
}

.subtitle {
  text-transform: uppercase;
  color: white;
}

.image {
  width: 100%;
  max-width: 1200px;
}

.nuggets {
  top: 240px;
  left: -120px;
  transform: rotate(65deg);
}

.chips {
  top: 45px;
  right: -120px;
  width: 240px;
}

@media screen and (max-width: 1128px) {
  .section-card-container {
    height: 620px;
  }

  .nuggets {
    display: none;
  }

  .chips {
    display: none;
  }
}

@media screen and (max-width: 768px) {
  .section-card-container {
    height: 500px;
  }

  .image {
    width: 80%;
    max-width: 1200px;
  }
}

@media screen and (max-width: 576px) {
  .section-card-container {
    height: 80vw;
  }

  .image {
    width: 80%;
    max-width: 1200px;
  }

  .title {
    font-size: 8vw;
  }

  .subtitle {
    font-size: 4vw;
  }
}
</style>
