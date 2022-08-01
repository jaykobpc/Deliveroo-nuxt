<template>
  <div class="productdescription no-select" role="presentation">
    <div class="productdescription__wrapper">
        <div role="img" class="productdescription__imagebox"></div>
        <div class="productdescription__context">
            <div class="productdescription__textview">
                <h3 class="productdescription__textview__title">B Bagel Bakery Bar - Tottenham Court Road</h3>
                <div class="productdescription__group">
                    <span>30 - 50 min · </span>
                    <span>Bagels · </span>
                    <span>Sandwiches · </span>
                    <span>Breakfast · </span>
                </div>
                <div class="listview__card__context__rating fs-16">
                  <i class="bx bxs-star"></i>
                  <span class="fs-16">4.8 Excellent</span>
                  <p class="fs-16">(500+)</p>
                </div>
                <div class="productdescription__group">
                    <span>Closes at 18:30 · </span>
                    <span>£3.99 delivery · </span>
                    <span>£7.00 minimum · </span>
                </div>
            </div>
            <div class="productdescription__orderinformation">
                <span role="img" class="productdescription__orderinformation__img"></span>
                <span class="productdescription__orderinformation__text">Deliver in 30 - 50 min</span>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductDescription",
};
</script>
