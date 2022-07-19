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
          <ListView title="Featured" subtitle="Paid placements from our partners" :dataset="NeighbourhoodData" />
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Home/Navbar.vue";
import GroupOptions from "@/components/Home/GroupOptions.vue";
import ListView from "@/components/Home/ListView.vue";

export default {
  name: "IndexPage",
  components: { Navbar, GroupOptions, ListView },
  computed: {
    NeighbourhoodData() {
      return this.$store.state.Neighbourhood;
    }
  }
};
</script>
