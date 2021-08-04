<template>
  <div>
    <Header />
    <Nuxt />
    <BottomNav />
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import BottomNav from "../components/BottomNav.vue";
export default {
  components: {
    Header,
    BottomNav
  }
};
</script>

<style></style>
