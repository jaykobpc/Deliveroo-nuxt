<template>
  <div class="restaurantview">
    <Navbar />
    <ProductDescription />
    <ProductScrollbox />
  </div>
</template>

<script>
import Navbar from "@/components/Navigation/Navbar.vue";
import ProductDescription from "@/components/Restaurant/ProductDescription.vue";
import ProductScrollbox from '@/components/Restaurant/ProductScrollbox.vue';

export default {
  name: "Restaurant",
  components: {
    Navbar,
    ProductDescription,
    ProductScrollbox,
  },
};
</script>
