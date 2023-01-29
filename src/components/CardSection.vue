<template>
  <div class="card">
    <div class="container">
      <div class="photo col">
        <img :src="product.image" />
      </div>
    </div>

    <div class="container">
      <div class="description col">
        <h1>{{ product.title }}</h1>

        <h4>{{ product.category }}</h4>
        <hr />
        <p>
          {{ product.description }}
        </p>
        <hr />
        <h1>$ {{ product.price }}</h1>
        <button class="buy">Buy Now</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WomanSection",
  props: ["product"],
};
</script>

<style>
</style>