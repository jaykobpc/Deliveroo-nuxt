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
    <div class="restaurantview__groupwrapper">
      <ProductGroupBox />
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navigation/Navbar.vue";
import ProductDescription from "@/components/Restaurant/ProductDescription.vue";
import ProductScrollbox from "@/components/Restaurant/ProductScrollbox.vue";
import ProductGroupBox from '@/components/Restaurant/ProductGroupBox.vue';

export default {
  name: "Restaurant",
  components: {
    Navbar,
    ProductDescription,
    ProductScrollbox,
    ProductGroupBox,
  },
  methods: {
    pushBack() {
      this.$router.push('/');
    }
  }
};
</script>
