<template>
  <div class="accordionlistview">
    <button
      @click.prevent="toggleAccordion"
      class="accordionlistview__togglebtn"
      :class="{ 'accordion__open': accordionOpen }">
      <span>{{ title }}</span>
      <i class="bx bx-chevron-down"></i>
    </button>
    <div v-if="accordionOpen" class="accordionlistview__grouplist">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  props: {
    title: {
      type: String,
      default: "Accordion title",
    },
    isOpen: {
      type: Boolean,
      default: false,
    }
  },
  data() {
    return {
      accordionOpen: this.isOpen,
    };
  },
  methods: {
    toggleAccordion() {
      return (this.accordionOpen = !this.accordionOpen);
    },
  },
};
</script>
