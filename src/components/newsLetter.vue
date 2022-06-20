<template>
  <div class="newsletter my-5">
    <div class="overlay"></div>
    <div class="m-4">
      <h2>Subscribe for New Updates!</h2>
      <p>
        When looking for a new bouquet idea for Valentines or Mother’s Day, ask us for a
        tip!
      </p>

      <div class="input-group input-group">
        <input
          type="text"
          class="form-control"
          aria-label=" "
          aria-describedby="inputGroup-sizing"
          placeholder="Enter your email"
        />
        <div class="input-group-prepend">
          <span class="input-group-text" id="inputGroup-sizing">Subscribe</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.newsletter {
  background-image: url("../assets/imgs/news.webp");
  height: 90vh;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  color: #fff;
  z-index: 2;
}

h2,
p {
  z-index: 2;
}
h2 {
  font-size: 5vw;
  margin-bottom: 10px;
}
p {
  font-size: 1.5vw;
  text-align: center;
}
.overlay {
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: -1;
}
input {
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
  padding: 10px;
}
.input-group-text {
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
  padding: 10px;
  background-color: #ef2853;
  color: #fff;
}
</style>
