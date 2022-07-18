<template>
  <div class="homeview" safe-area-view="yes">
    <div class="homeview__layout">
      <navbar />
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Home/Navbar.vue'

export default {
  components: { Navbar },
  name: 'IndexPage'
}
</script>
