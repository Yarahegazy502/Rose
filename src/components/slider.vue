<template>
  <div class="sliders">
    <div class="sliderContent text-center">
      <strong>Welcome to my Rose</strong>
      <h1>PERFECT BOUQUET</h1>
      <p>
        A simply gorgeous WordPress theme packed with everything you will need to create a
        delightful website for your flower shop or florist business quickly and with ease.
      </p>
    </div>
    <div>
      <b-carousel
        id="carousel-fade"
        style="text-shadow: 0px 0px 2px #000"
        fade
        indicators
        img-width="1024"
        img-height="480"
        :interval="3000"
      >
        <b-carousel-slide
          img-src="https://rosebud.qodeinteractive.com/wp-content/uploads/2018/02/h1-slide-1.jpg"
        >
        </b-carousel-slide>

        <b-carousel-slide
          img-src="https://rosebud.qodeinteractive.com/wp-content/uploads/2018/02/h1-slide-2.jpg"
        >
        </b-carousel-slide>

        <b-carousel-slide
          img-src="https://rosebud.qodeinteractive.com/wp-content/uploads/2018/02/h1-slide-3.jpg"
        >
        </b-carousel-slide>
      </b-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    // onSlideStart(slide) {
    //   this.sliding = true;
    // },
    // onSlideEnd(slide) {
    //   this.sliding = false;
    // },
  },
};
</script>
<style>
#carousel-fade {
  margin-bottom: 30px;
}
.sliders {
  position: relative;
}
.sliderContent {
  position: absolute;
  top: 50%;
  color: #fff;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  line-height: 2;
}
.sliderContent strong {
  font-family: "Bodoni Moda", serif;
  font-size: 4vw;
}
.sliderContent h1 {
  font-size: 5vw;
}
.sliderContent p {
  font-size: 1.5vw;
}
</style>
