<template>
  <div class="input-slider">
    <div class="input-slider__label">{{ label }}</div>
    <div class="input-slider__display">
      <template v-if="isPrice == true">
        {{ value | formatCurrency }}
      </template>
      <template v-else>
        {{ value }} {{ suffix }}
      </template>
    </div>
    <input
      type="range"
      :min="min"
      :max="max"
      v-bind:value="value"
      v-on:input="$emit('input', $event.target.value)"
      class="input-slider__slider">
  </div>
</template>

<script>
export default {
  props: [ 'value', 'label', 'type', 'suffix', 'isPrice', 'min', 'max'  ],
}
</script>

<style lang="scss" src="./j-input-slider.scss"></style>