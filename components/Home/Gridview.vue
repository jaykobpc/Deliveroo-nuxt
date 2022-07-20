<template>
  <div class="gridview">
    <h3 v-if="title" class="gridview__title">{{ title }}</h3>
    <div class="gridview__wrapper">
      <div v-for="(item, index) in dataset" :key="index" class="gridview__card listview__card">
        <div class="listview__card__imagebox">
          <span class="listview__card__imagebox__badge">
            <p>{{ item.deliveryFee }}</p>
          </span>
          <span
            :style="`background-image: url(${require(`@/static/Restaurants/${item.restaurantLogo}`)})`"
            class="listview__card__imagebox__img"
          ></span>
          <div class="listview__card__imagebox__timestamp">
            <span>
              <i class="bx bxs-timer"></i>
            </span>
            <span>{{ item.duration }} min</span>
          </div>
        </div>
        <div class="listview__card__context">
          <h3 class="listview__card__context__title">
            {{ item.restaurantName }}
          </h3>
          <div class="listview__card__context__rating">
            <i class="bx bxs-star"></i>
            <span>{{ item.rating }}</span>
            <p>({{ item.ratingCount }})</p>
          </div>
          <div class="listview__card__delivery">
            <span class="listview__card__delivery__pin">
              <i class="bx bx-map-pin"></i>
              <span>{{ item.locationDistance }} · &nbsp;</span>
            </span>
            <span class="listview__card__delivery__price">
              {{ item.deliveryFee }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Gridview",
  props: {
    title: {
        type: String,
    },
    dataset: {
        type: Array,
        required: true,
    }
  }
};
</script>
