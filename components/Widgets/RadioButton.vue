<template>
  <label :for="title" class="sidebarlocation__radiogroup__radiobtn no-select">
    <input
      type="radio"
      :name="name"
      :value="title"
      :id="title"
      :checked="checked"
      class="sidebarlocation__radiogroup__radio"
    />
    <span class="sidebarlocation__radiogroup__text">{{ title }}</span>
  </label>
</template>

<script>
export default {
  name: "RadioButton",
  props: {
    title: {
      type: String,
      default: "RadioButton",
    },
    name: {
      type: String,
      default: "radio-group",
    },
    checked: {
      type: Boolean,
      default: true,
    },
  },
};
</script>
