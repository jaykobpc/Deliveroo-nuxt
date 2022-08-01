<template>
  <div class="restaurantview">
    <Navbar />
    <div class="restaurantview__nav">
      <button @click="pushBack" class="restaurantview__nav__button">
        <i class="bx bx-left-arrow-alt"></i>
      </button>
    </div>
    <ProductDescription />
    <ProductScrollbox />
  </div>
</template>

<script>
import Navbar from "@/components/Navigation/Navbar.vue";
import ProductDescription from "@/components/Restaurant/ProductDescription.vue";
import ProductScrollbox from "@/components/Restaurant/ProductScrollbox.vue";

export default {
  name: "Restaurant",
  components: {
    Navbar,
    ProductDescription,
    ProductScrollbox,
  },
  methods: {
    pushBack() {
      this.$router.push('/');
    }
  }
};
</script>
