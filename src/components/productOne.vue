<template>
  <div>
    <div class="product shadow rounded p-4">
      <div>
        <div class="productImg"><img :src="img" /></div>
        <div>
          <p>{{ title }}</p>
          <button class="btn">add to cart</button>
          <button
            class="btn hearticon"
            :class="[btn, hearticon, isFavorite ? 'fav' : '']"
            @click="$emit('addToHeart'), favoriteHeart()"
          >
            {{ isFavorite ? "❤" : "🤍" }}
            <!-- <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-heart"
              viewBox="0 0 16 16"
            >
              <path
                d="m8 2.748-.717-.737C5.6.281 2.514.878 1.4 3.053c-.523 1.023-.641 2.5.314 4.385.92 1.815 2.834 3.989 6.286 6.357 3.452-2.368 5.365-4.542 6.286-6.357.955-1.886.838-3.362.314-4.385C13.486.878 10.4.28 8.717 2.01L8 2.748zM8 15C-7.333 4.868 3.279-3.04 7.824 1.143c.06.055.119.112.176.171a3.12 3.12 0 0 1 .176-.17C12.72-3.042 23.333 4.867 8 15z"
              />
            </svg> -->
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title", "img", "isFavorite"],
  data() {
    return {};
  },
  methods: {
    favoriteHeart() {
      this.isFavorite = !this.isFavorite;
    },
  },
};
</script>

<style scoped>
.productImg img {
  width: 100%;
  transition: all 0.3s ease in out;
  transform: scale(1.2);
}
.fav {
  background-color: #ef2853;
}
.product {
  margin: 20px 0;
  overflow: hidden;
}
.product button {
  background-color: #ef2853;
  border: 0;
  border-radius: 7px;
  padding: 5px 15px;
  color: #fff;
}
.product .hearticon {
  float: right;
}
.product p {
  margin-top: 5px;
}
.productImg {
  overflow: hidden;
  transition: all 0.3s ease in out;
}
.product .productImg img:hover {
  transform: scale(1);
}
</style>
