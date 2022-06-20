<template>
  <div id="app">
    <navbar :counter1="0" />
    <foot />
  </div>
</template>

<script>
import navbar from "@/components/layout/navbar.vue";
import foot from "@/components/layout/footer.vue";

export default {
  components: {
    navbar,
    foot,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Bodoni+Moda:opsz,wght@6..96,400;6..96,500;6..96,600;6..96,700;6..96,800;6..96,900&family=Gwendolyn:wght@400;700&family=Open+Sans:wght@300;400;500;600;700;800&family=Poppins:ital,wght@0,200;0,400;1,600&display=swap");
</style>
