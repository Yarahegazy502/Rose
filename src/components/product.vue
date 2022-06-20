<template>
  <div class="container">
    <button class="btn btn-danger px-3" @click="isproduct = !isproduct" v-if="!isproduct">
      add new product
    </button>
    <add-product @addProduct="add" v-if="isproduct" @back="isproduct = false" />

    <div class="row" v-if="!isproduct">
      <!-- <div class="col-md-3" v-for="p in prds" :key='p'>
                <div v-if="isFavourite">
                    <img :src="p.url"/>
                <p>{{p.title}}</p>
                <button>add to cart</button>
                <button @click='isFavourite=!isFavourite'>❤</button>
                </div>
            </div> -->
      <productOne
        class="col-lg-3 col-md-6"
        v-for="p in prds"
        :key="p"
        :title="p.title"
        :img="p.url"
        :is-favorite="0"
      />
    </div>
  </div>
</template>

<script>
import productOne from "@/components/productOne.vue";
import addProduct from "@/components/addProduct.vue";
import axios from "axios";
export default {
  data() {
    return {
      //   isFavourite: true,
      prds: [],
      isproduct: false,
    };
  },
  // methods: {},
  methods: {
    async add(pro) {
      const res = await axios.post("http://localhost:3000/prds", pro);
      this.prds = [...this.prds, res.data];
    },
  },

  async created() {
    try {
      const res = await axios.get("http://localhost:3000/prds");
      this.prds = res.data;
    } catch (e) {
      console.error(e);
    }
  },

  components: {
    productOne,
    addProduct,
  },
};
</script>
