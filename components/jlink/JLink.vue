<template>
  <a
    class="link"
    :class="{
      'link--hover-color': hoverType == 'color',
      'link--hover-underline': hoverType == 'underline'
    }"
    :to="to"
  >
    <slot></slot>
  </a>
</template>

<script>
export default {
  props: {
    to: {
      type: String,
      default: ''
    },
    hoverType: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" src="./jlink.scss"></style>