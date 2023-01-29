<template>
  <div class="container">
    <div class="row">
      <div v-for="product in products" :key="product.id">
        <CardSection :product="product" />
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import CardSection from "@/components/CardSection.vue";

export default {
  name: "ProductDisplay",
  components: {
    CardSection,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get("https://fakestoreapi.com/products")
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
@import "../assets/style/card.css";
</style>