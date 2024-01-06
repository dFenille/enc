<template>
  <div id="gallery" class="bg-blue-solid">
    <CardContainer>
      <template v-slot:content>
        <div
          class="section-card-container d-flex flex-column justify-content-center align-items-center w-100"
        >
          <div class="title-container">
            <h1 class="section-title">Compre, junte e troque</h1>
          </div>

          <div
            class="tabs-container d-flex justify-content-between align-items-center w-100"
          >
            <div
              v-for="tab in tabs"
              :key="tab.id"
              class="tab d-flex align-items-center"
              :class="
                selectedTab && selectedTab.id === tab.id && 'selected-tab'
              "
              @click="selectedTab = tab"
            >
              {{ tab.text }}
            </div>
          </div>

          <div class="desktop-img-container pt-5">
            <img
              :src="require(`../assets/gallery/${selectedTab.desktopImg}.png`)"
              alt=""
              class="w-100"
            />
          </div>

          <div class="mobile-img-container pt-4">
            <img
              :src="require(`../assets/gallery/${selectedTab.mobileImg}.png`)"
              alt=""
              class="w-100"
            />
          </div>
        </div>
      </template>
    </CardContainer>
  </div>
</template>

<script>
import CardContainer from "@/components/CardContainer.vue";

export default {
  name: "GallerySection",

  components: {
    CardContainer,
  },

  data() {
    return {
      tabs: [
        {
          id: 1,
          text: "Pratos",
          desktopImg: "galeria-pratos",
          mobileImg: "galeria-pratos-mob",
        },
        {
          id: 2,
          text: "Bowls",
          desktopImg: "galeria-bowls",
          mobileImg: "galeria-bowls-mob",
        },
        {
          id: 3,
          text: "Tábua",
          desktopImg: "galeria-tabua",
          mobileImg: "galeria-tabua-mob",
        },
      ],

      selectedTab: null,
    };
  },

  created() {
    this.selectedTab = this.tabs[0];
  },
};
</script>

<style scoped>
#gallery {
  font-family: "BrandonGrotesqueBlack", sans-serif;
  text-transform: uppercase;
}

.mobile-img-container {
  display: none;
}

.section-card-container {
  padding: 38px 148px;
}

.title-container {
  padding-bottom: 16px;
}

.section-title {
  font-size: 34px;
  color: var(--secondary-color);
}

.tabs-container {
  background-color: var(--primary-color);
  border-radius: 40px;
  height: 44px;
  padding: 8px;
  width: 100%;
  max-width: 580px;
}

.tab {
  font-family: "BrandonGrotesqueBlack", sans-serif;
  color: white;
  text-transform: uppercase;
  border: none;
  border-radius: 44px;
  height: 44px;
  padding: 0 44px;
  font-size: 20px;
  cursor: pointer;
}

.selected-tab {
  background-color: var(--secondary-color);
  color: var(--primary-color);
}

@media screen and (max-width: 768px) {
  .desktop-img-container {
    display: none;
  }

  .mobile-img-container {
    display: block;
  }

  .section-card-container {
    padding: 38px 24px;
  }

  .section-title {
    font-size: 24px;
  }

  .tabs-container {
    border-radius: 36px;
    height: 36px;
    padding: 8px;
  }

  .tab {
    border-radius: 44px;
    height: 36px;
    padding: 0 16px;
    font-size: 16px;
    cursor: pointer;
  }
}
</style>
