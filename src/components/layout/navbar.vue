<template>
  <div>
    <div class="nnavbar">
      <b-navbar toggleable="lg" class="container">
        <b-navbar-brand href="#" class="text-danger"> Rose </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item class="active" to="/">Home</b-nav-item>
            <b-nav-item to="/about">About</b-nav-item>
            <b-nav-item-dropdown text="Services" right> </b-nav-item-dropdown>
            <b-nav-item to="/Works">Blog</b-nav-item>
            <b-nav-item to="/Contact">Contact Us</b-nav-item>
          </b-navbar-nav>
        </b-collapse>

        <div class="cartAndHeartIcon">
          <span class="cart"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="21"
              height="21"
              fill="currentColor"
              class="bi bi-basket"
              viewBox="0 0 16 16"
            >
              <path
                d="M5.757 1.071a.5.5 0 0 1 .172.686L3.383 6h9.234L10.07 1.757a.5.5 0 1 1 .858-.514L13.783 6H15a1 1 0 0 1 1 1v1a1 1 0 0 1-1 1v4.5a2.5 2.5 0 0 1-2.5 2.5h-9A2.5 2.5 0 0 1 1 13.5V9a1 1 0 0 1-1-1V7a1 1 0 0 1 1-1h1.217L5.07 1.243a.5.5 0 0 1 .686-.172zM2 9v4.5A1.5 1.5 0 0 0 3.5 15h9a1.5 1.5 0 0 0 1.5-1.5V9H2zM1 7v1h14V7H1zm3 3a.5.5 0 0 1 .5.5v3a.5.5 0 0 1-1 0v-3A.5.5 0 0 1 4 10zm2 0a.5.5 0 0 1 .5.5v3a.5.5 0 0 1-1 0v-3A.5.5 0 0 1 6 10zm2 0a.5.5 0 0 1 .5.5v3a.5.5 0 0 1-1 0v-3A.5.5 0 0 1 8 10zm2 0a.5.5 0 0 1 .5.5v3a.5.5 0 0 1-1 0v-3a.5.5 0 0 1 .5-.5zm2 0a.5.5 0 0 1 .5.5v3a.5.5 0 0 1-1 0v-3a.5.5 0 0 1 .5-.5z"
              />
            </svg>
            <span @addToHeart="addTHeart()">{{ counter1 }}</span>
          </span>
          <span class="heart">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="21"
              height="21"
              fill="currentColor"
              class="bi bi-heart"
              viewBox="0 0 16 16"
            >
              <path
                d="m8 2.748-.717-.737C5.6.281 2.514.878 1.4 3.053c-.523 1.023-.641 2.5.314 4.385.92 1.815 2.834 3.989 6.286 6.357 3.452-2.368 5.365-4.542 6.286-6.357.955-1.886.838-3.362.314-4.385C13.486.878 10.4.28 8.717 2.01L8 2.748zM8 15C-7.333 4.868 3.279-3.04 7.824 1.143c.06.055.119.112.176.171a3.12 3.12 0 0 1 .176-.17C12.72-3.042 23.333 4.867 8 15z"
              />
            </svg>
            <span>{{ c2 }}</span>
          </span>
        </div>
      </b-navbar>
      <router-view />
    </div>
  </div>
</template>

<script>
// import productOne from "@/components/productOne.vue";

export default {
  // props: ["counter1"],
  data() {
    return {
      // c1: 0,
      counter1: 0,
      c2: 0,
    };
  },
  methods: {},
  // components: {
  //   productOne,
  // },
};
</script>

<style scoped>
.nnavbar {
  /* position: fixed; */
  width: 100%;
  top: 0;
}
img {
  width: 200px;
}
.navbar-nav {
  margin: auto;
}

.navbar ul li {
  margin: 0 5px;
  font-size: 16px;
}
.navbar-light .navbar-nav .nav-link {
  color: #000;
}
.navbar-light .navbar-nav .nav-link:hover {
  color: #fa1f1f;
}
.navbar-light .navbar-nav .nav-link.active {
  color: #fa1f1f;
}
.cartAndHeartIcon .cart,
.cartAndHeartIcon .heart {
  margin: 15px;
  position: relative;
}
.cartAndHeartIcon .cart span,
.cartAndHeartIcon .heart span {
  background-color: #ef2853;
  width: 20px;
  height: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  color: #fff;
  position: absolute;
  top: -5px;
  right: -12px;
  cursor: pointer;
}

/* .navbar-nav .dropdown-menu {
  position: absolute;
  width: 60vw;
  left: -250px;
  text-align: right;
  padding: 20px;
}
.dropdown2 {
  margin: 20px;
}
.dropdown2 h5, */
/* .dropdown2 hr {
  color: #fa1f1f;
}
.dropdown2 li a {
  text-decoration: none;
  color: #000;
}
.dropdown2 li {
  padding-bottom: 5px;
  transition: all 0.3s ease-in-out;
}
.dropdown2 li:hover {
  transform: translateX(-10px);
}
.dropIcon{
  float: left;
  margin-top: 7px;
} */
</style>
