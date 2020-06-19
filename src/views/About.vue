<template>
  <div class="about">
    <HeaderJfcollection />
      <h1>This is an about page</h1>
    <FooterJfcollection />
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderJfcollection from "@/components/HeaderJfcollection.vue";
import FooterJfcollection from "@/components/FooterJfcollection.vue";

export default {
  name: "About",
  components: {
    HeaderJfcollection,
    FooterJfcollection
  }
};
</script>
