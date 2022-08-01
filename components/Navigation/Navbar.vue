<template>
  <nav role="navigation" class="navbar no-select">
    <div class="navbar__wrapper">
      <!-- mobile -->
      <div class="navbar__toplayer">
        <div role="button" class="navbar__locationbtn">
          <div class="navbar__locationbtn__logo"></div>
          <div class="navbar__locationbtn__textbox">
            <span class="navbar__locationbtn__textbox__smtitle">Delivery · Now</span>
            <h3 class="navbar__locationbtn__textbox__title">
              Selected location
            </h3>
          </div>
         <span class="navbar__locationbtn__icon">
           <i class='bx bx-chevron-down'></i>
         </span>
        </div>
        <div class="navbar__profilebox">
          <img src="@/static/Profiles/user_1.jpg" draggable="false" alt="Profile Image" class="navbar__profilebox__img">
        </div>
      </div>
      <!-- desktop -->
      <div class="navbar__bottomlayer">
        <div role="img" class="navbar__bottomlayer__brandlogo"></div>
        <div class="navbar__bottomlayer__searchbox">
         <div class="navbar__bottomlayer__inputbox">
           <i class='navbar__bottomlayer__inputbox__icon bx bx-search' ></i>
           <input type="text" placeholder="Restaurants, groceries, dishes" class="navbar__bottomlayer__inputbox__input">
         </div>
         <span class="navbar__bottomlayer__searchbox__icon">
            <i class='bx bx-slider-alt'></i>
         </span>
        </div>
        <div class="navbar__bottomlayer__widgets">
          <div role="button" class="navbar__bottomlayer__navbtn">
            <i class='bx bx-basket' ></i>
            <span>£0.00</span>
          </div>
          <div role="button" class="navbar__bottomlayer__navbtn">
           <i class='bx bx-menu' ></i>
            <span>Menu</span>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  name: "Navbar",
  data() {
    return {
     
    };
  },
};
</script>