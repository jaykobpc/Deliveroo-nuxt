<template>
  <div role="presentation" class="productscrollbox">
    <div class="productscrollbox__wrapper">
      <span
        v-for="(item, index) in groups"
        :key="index"
        class="productscrollbox__badge"
      >
        <span class="productscrollbox__badge__text">{{ item }}</span>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductScrollbox",
  data() {
    return {
      groups: [
        "Meal Deals",
        "Build Your Own",
        "Signature Specials",
        "Kids Pizza",
        "Calzone",
        "Slides",
        "Dessert",
        "Milkshakes",
        "Drinks",
      ],
    };
  },
};
</script>
