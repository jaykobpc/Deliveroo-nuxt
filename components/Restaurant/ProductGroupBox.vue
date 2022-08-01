<template>
  <div class="productgroupbox">
    <h3 class="productgroupbox__title">Meal Deals</h3>
    <div class="productgroupbox__gridview">
        <GroupBoxCard />
    </div>
  </div>
</template>

<script>
import GroupBoxCard from './GroupBoxCard.vue';

export default {
    name: 'ProductGroupBox',
    components: {
        GroupBoxCard,
    }
}
</script>
