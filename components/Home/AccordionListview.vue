<template>
  <div class="accordion__column">
    <Accordion title="Sort" :isOpen="true">
      <RadioButton title="Distance" name="sort-group" :checked="true" />
      <RadioButton title="Hygiene ratings" name="sort-group" :checked="false" />
      <RadioButton title="Quickest delivery" name="sort-group" :checked="false" />
      <RadioButton title="Recommended" name="sort-group" :checked="false" />
      <RadioButton title="Top rated" name="sort-group" :checked="false" />
    </Accordion>
    <Accordion title="Hygiene rating">
      <CheckBox title="Hygiene rating: 5" name="hygiene-rating" :checked="true" />
      <CheckBox title="Hygiene rating: 4" name="hygiene-rating" :checked="false" />
      <CheckBox title="Hygiene rating: 3" name="hygiene-rating" :checked="false" />
      <CheckBox title="Hygiene rating: 2" name="hygiene-rating" :checked="false" />
    </Accordion>
    <Accordion title="Offers" :isOpen="false">
      <RadioButton title="All Offers" name="offers-group" :checked="true" />
      <RadioButton title="Offers near you" name="offers-group" :checked="false" />
      <RadioButton title="Restaurant picks" name="offers-group" :checked="false" />
      <RadioButton title="Order more, save more" name="offers-group" :checked="false" />
      <RadioButton title="Flash deals" name="offers-group" :checked="false" />
      <RadioButton title="Free Items" name="offers-group" :checked="false" />
      <RadioButton title="Free Delivery" name="offers-group" :checked="false" />
    </Accordion>
  </div>
</template>

<script>
import RadioButton from "@/components/Widgets/RadioButton.vue";
import CheckBox from '@/components/Widgets/Checkbox.vue';
import Accordion from "@/components/Widgets/Accordion.vue";

export default {
  name: "AccordionListView",
  components: {
    CheckBox,
    Accordion,
    RadioButton,
  },
};
</script>
