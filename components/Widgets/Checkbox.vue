<template>
  <label :for="title" class="checkbox__radiogroup__radiobtn no-select">
    <input
      type="checkbox"
      :name="name"
      :value="title"
      :id="title"
      :checked="checked"
      class="checkbox__radiogroup__radio"
    />
    <span class="checkbox__radiogroup__text">{{ title }}</span>
  </label>
</template>

<script>
export default {
  name: "Checkbox",
  props: {
    name: {
      type: String,
      default: "Checkbox",
    },
    title: {
      type: String,
      default: "Checkbox",
    },
    checked: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
