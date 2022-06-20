<template>
  <div>
    <button class="btn btn-danger px-3 mb-4" @click="$emit('back')">back</button>
    <form @submit="submit">
      <div>
        <input
          type="text"
          class="form-control mb-3"
          placeholder="Enter URL of img"
          aria-describedby="basic-addon1"
          v-model="url"
        />
      </div>

      <div>
        <textarea
          class="form-control textArea mb-3"
          aria-label="With textarea"
          placeholder="Enter Desription"
          v-model="title"
        ></textarea>
      </div>

      <button type="submit" class="btn btn-danger px-4">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "",
      url: "",
    };
  },
  methods: {
    submit(e) {
      e.preventDefault();
      const newProduct = {
        url: this.url,
        title: this.title,
      };
      console.log(newProduct);

      this.$emit("addProduct", newProduct);

      this.url = "";
      this.title = "";
    },
  },
};
</script>

<style>
.textArea {
  white-space: pre;
}
</style>
