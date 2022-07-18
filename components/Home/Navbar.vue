<template>
  <nav class="navbar">
    <div class="navbar__wrapper">
      <div class="navbar__toplayer">
        <div role="button" class="navbar__locationbtn">
          <div class="navbar__locationbtn__logo"></div>
          <div class="navbar__locationbtn__textbox">
            <span class="navbar__locationbtn__textbox__smtitle">Delivery . Now</span>
            <h3 class="navbar__locationbtn__textbox__title">
              Selected location
            </h3>
          </div>
          <Swiper :options="swiperOptions">
            <SwiperSlide>
              <button>Hello world!</button>
            </SwiperSlide>
          </Swiper>
        </div>
      </div>
      <div class="navbar__bottomlayer">
        <span>bottom</span>
      </div>
    </div>
  </nav>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
export default {
  name: "Navbar",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      swiperOptions: {
        slidesPerView: 5,
        spaceBetween: 30,
        freeMode: true,
        loop: false,
      },
    };
  },
};
</script>u