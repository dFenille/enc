<template>
  <div id="app">
    <TheHeader />
    <HomeSection />
    <PrizesSection />
    <HowToParticipateSection />
    <GallerySection />
    <VideoSection />
    <ProductsSection />
    <BuyNowSection />
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import HomeSection from "./views/HomeSection.vue";
import PrizesSection from "./views/PrizesSection.vue";
import HowToParticipateSection from "./views/HowToParticipateSection.vue";
import GallerySection from "./views/GallerySection.vue";
import VideoSection from "./views/VideoSection.vue";
import ProductsSection from "./views/ProductsSection.vue";
import BuyNowSection from "./views/BuyNowSection.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    HomeSection,
    PrizesSection,
    HowToParticipateSection,
    GallerySection,
    VideoSection,
    ProductsSection,
    BuyNowSection,
    TheFooter,
  },
};
</script>

<style>
:root {
  --primary-color: #074a75;
  --primary-dark-color: #122641;
  --secondary-color: #facc1f;
}

@font-face {
  font-family: "BrandonGrotesqueBlack";
  src: url("./assets/fonts/Brandon Grotesque Black.otf") format("opentype");
}

@font-face {
  font-family: "TrendSansFive";
  src: url("./assets/fonts/Latinotype - TrendSansFive.otf") format("opentype");
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  box-sizing: border-box;
  overflow: hidden;
}

.fill-height {
  height: 100vh;
}

.bg-blue-img {
  background-image: url("./assets/bg-azul.jpg");
}

.bg-blue-solid {
  background-color: var(--primary-color);
}

.bg-blue-dark-solid {
  background-color: var(--primary-dark-color);
}
</style>
