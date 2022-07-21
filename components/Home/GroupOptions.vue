<template>
  <div class="groupoptions">
    <div class="groupoptions__wrapper no-select">
      <h3 class="groupoptions__title">Delivering to The City</h3>
      <Swiper :options="swiperOptions">
        <SwiperSlide v-for="(item, index) in GroupOptions" :key="index">
          <div class="groupoptions__imagebox">
            <div
              :style="`background-image: url(${require(`@/static/GroupA/${item.img}`)})`"
              draggable="false"
              role="image"
              class="groupoptions__imagebox__img">
            </div>
            <span class="groupoptions__imagebox__text">{{ item.title }}</span>
          </div>
        </SwiperSlide>
      </Swiper>
      <div role="button" id="groupOptionNext" class="groupoptions__rightbtn">
        <i class='bx bx-right-arrow-alt'></i>
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";

export default {
  name: "GroupOptions",
  components: {
    Swiper,
    SwiperSlide,
  },
  computed: {
    GroupOptions() {
      return this.$store.state.GroupOptions;
    },
  },
  data() {
    return {
      swiperOptions: {
        slidesPerView: 8,
        spaceBetween: 10,
        freeMode: true,
        loop: false,
        breakpoints: {
          1440: {
            slidesPerView: 8,
            spaceBetween: 10,
          },
          1024: {
            slidesPerView: 4,
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
            slidesPerView: 3,
            spaceBetween: 10,
          },
        },
        navigation: {
          nextEl: "#groupOptionNext",
          prevEl: "#groupOptionPrev",
        },
      },
    };
  },
};
</script>