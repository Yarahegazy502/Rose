<template>
  <div class="home">
    <!-- <product-one/> -->
    <slider />
    <product />
    <shop />
    <bouquet />
    <newsLetter />
    <!-- <contact/>
    <contactUs/> -->
  </div>
</template>

<script>
// @ is an alias to /src
import slider from "@/components/slider.vue";
import product from "@/components/product.vue";
import shop from "@/components/shop.vue";
import bouquet from "@/components/bouquet.vue";
import newsLetter from "@/components/newsLetter.vue";
// import productOne from '@/components/productOne.vue'
// import contact from '@/components/contact.vue'
// import contactUs from '@/components/contactUs.vue'

export default {
  name: "Home",
  components: {
    slider,
    product,
    shop,
    bouquet,
    newsLetter,
    // productOne
    // contact,
    // contactUs,
  },
};
</script>

<style>
h2 {
  text-align: center;
}
</style>
