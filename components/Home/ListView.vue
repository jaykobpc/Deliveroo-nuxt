<template>
  <div class="listview">
    <div class="listview__wrapper">
      <h3 class="listview__title">{{ title }}</h3>
      <h4 class="listview__subtitle">{{ subtitle }}</h4>
      <div class="listview__swiper">
        <Swiper :options="swiperOptions">
          <SwiperSlide v-for="(item, index) in dataset" :key="index">
            <router-link to="/restaurant" class="listview__card">
              <div class="listview__card__imagebox">
                <span class="listview__card__imagebox__badge">
                  <p>{{ item.deliveryFee }}</p>
                </span>
                <span
                  :style="`background-image: url(${require(`@/static/Restaurants/${item.restaurantLogo}`)})`"
                  class="listview__card__imagebox__img">
                </span>
                <div class="listview__card__imagebox__timestamp">
                  <span>
                    <i class="bx bxs-timer"></i>
                  </span>
                  <span class="text-gray-600">{{ item.duration }} min</span>
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
            </router-link>
          </SwiperSlide>
        </Swiper>
      </div>
      <!-- scrollbtn -->
      <div
        v-if="dataset.length > 5"
        role="button"
        :id="scrollNextId"
        class="listview__wrapper__rightbtn"
      >
        <i class="bx bx-right-arrow-alt"></i>
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";

export default {
  name: "ListView",
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
    title: {
      type: String,
      required: true,
      default: "Title is required",
    },
    subtitle: {
      type: String,
    },
    dataset: {
      type: Array,
      required: true,
    },
    scrollNextId: {
      type: String,
    },
  },
  data() {
    return {
      swiperOptions: {
        slidesPerView: 3,
        spaceBetween: 15,
        freeMode: true,
        loop: false,
        breakpoints: {
          1440: {
            slidesPerView: 6,
            spaceBetween: 15,
          },
          1024: {
            slidesPerView: 5,
            spaceBetween: 10,
          },
          768: {
            slidesPerView: 3,
            spaceBetween: 10,
          },
          640: {
            slidesPerView: 2,
            spaceBetween: 10,
          },
          320: {
            slidesPerView: 1,
            spaceBetween: 10,
          },
        },
        navigation: {
          nextEl: `#${this.scrollNextId}`,
          prevEl: "#groupOptionPrev",
        },
      },
    };
  },
};
</script>
