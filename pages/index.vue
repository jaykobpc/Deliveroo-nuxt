<template>
  <div class="homeview" safe-area-view="yes">
    <div class="homeview__wrapper">
      <navbar />
      <div class="homeview__layout">
        <aside class="homeview__layout__sidebar">
          <h3>Sidebar</h3>
        </aside>
        <section class="homeview__layout__main">
          <GroupOptions />
          <ListView title="Top picks in your neighbourhood"  :dataset="NeighbourhoodData" />
          <ListView title="Featured" subtitle="Paid placements from our partners" :dataset="FeaturedData" scrollNextId="featuredBtn" />
          <ListView title="Offers near you" :dataset="FeaturedData" scrollNextId="OffersBtn" />
          <GridView title="Popular brands" :dataset="Populargrid" />
          <ListView title="Meal deals" :dataset="FeaturedData" scrollNextId="mealDealsBtn" />
          <GridView :dataset="Populargrid" />
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Home/Navbar.vue";
import GroupOptions from "@/components/Home/GroupOptions.vue";
import ListView from "@/components/Home/ListView.vue";
import GridView from '@/components/Home/Gridview.vue';

export default {
  name: "IndexPage",
  components: { Navbar, GroupOptions, ListView, GridView, },
  computed: {
    NeighbourhoodData() {
      return this.$store.state.Neighbourhood;
    },
    FeaturedData() {
      return this.$store.state.Featured;
    },
    Populargrid() {
      return this.$store.state.PopularGrid;
    }
  }
};
</script>
