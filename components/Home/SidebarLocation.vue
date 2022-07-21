<template>
  <div class="sidebarlocation">
    <div role="button" class="sidebarlocation__pickerbtn">
        <div class="sidebarlocation__pickerbtn__group">
            <span class="sidebarlocation__pickerbtn__img"></span>
            <span class="sidebarlocation__pickerbtn__textview">
                <p>Now</p>
                <h3>Holland Park</h3>
            </span>
        </div>
        <span class="sidebarlocation__pickerbtn__text">Change</span>
    </div>
    <div class="sidebarlocation__radiogroup">
        <RadioButton title="Delivery" name="radio-group" :checked="true" />
        <RadioButton title="Pickup" name="radio-group" :checked="false" />
        <RadioButton title="Table Service" name="radio-group" :checked="false" />
    </div>
  </div>
</template>

<script>
import RadioButton from '@/components/Widgets/RadioButton.vue';

export default {
    name: 'SidebarLocation',
    components: {
        RadioButton,
    }
}
</script>
