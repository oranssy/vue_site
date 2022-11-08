<template>
  <HeaderLayout fonts="nexon" />
  <SliderSection fonts="nexon" />
  <ImageSection attr="section nexon" layout="container" />
  <ImageTextSection attr="nexon section gray" layout="container" />
  <CardSection attr="section nexon" layout="container" />
  <BannerSection fonts="nexon" />
  <TextSection attr="nexon section" layout="container" />
  <FooterLayout attr="nexon section gray" layout="container" />
</template>

<script>
import HeaderLayout from "./components/layout/HeaderLayout.vue";
import SliderSection from "./components/section/SliderSection.vue";
import ImageSection from "./components/section/ImageSection.vue";
import ImageTextSection from "./components/section/ImageTextSection.vue";
import CardSection from "./components/section/CardSection.vue";
import BannerSection from "./components/section/BannerSection.vue";
import TextSection from "./components/section/TextSection.vue";
import FooterLayout from "./components/layout/FooterLayout.vue";

export default {
  name: "App",
  components: {
    HeaderLayout,
    SliderSection,
    ImageSection,
    ImageTextSection,
    CardSection,
    BannerSection,
    TextSection,
    FooterLayout,
  },
};
</script>

<style></style>
