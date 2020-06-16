<template>
  <div class="home">
    <HeaderJfcollection />
    <HeroJfcollection />
    <BannerJfcollection />
    <InstaJfcollection />
    <PartnerJfcollection />
    <FooterJfcollection />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import HeaderJfcollection from "@/components/HeaderJfcollection.vue";
import HeroJfcollection from "@/components/HeroJfcollection.vue";
import BannerJfcollection from "@/components/BannerJfcollection.vue";
import InstaJfcollection from "@/components/InstaJfcollection.vue";
import PartnerJfcollection from "@/components/PartnerJfcollection.vue";
import FooterJfcollection from "@/components/FooterJfcollection.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld
    HeaderJfcollection,
    HeroJfcollection,
    BannerJfcollection,
    InstaJfcollection,
    PartnerJfcollection,
    FooterJfcollection
  }
};
</script>
