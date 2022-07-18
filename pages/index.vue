<template>
  <div class="homeview" safe-area-view="yes">
    <div class="homeview__wrapper">
      <navbar />
      <div class="homeview__layout">
        <section class="homeview__layout__sidebar">
          <h3>Sidebar</h3>
        </section>
        <section class="homeview__layout__main">
          <h3>main section</h3>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Home/Navbar.vue'

export default {
  name: 'IndexPage',
  components: { Navbar },
}
</script>
