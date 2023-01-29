<template>
  <div class="home">
   <ProductDisplay/>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductDisplay from './ProductDisplay.vue';

export default {
  name: 'HomeView',
  components: {
    ProductDisplay,
}
}
</script>
