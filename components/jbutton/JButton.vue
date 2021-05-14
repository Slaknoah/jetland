<template>
  <a :to="to" class="btn">
    <slot></slot>
  </a>
</template>

<script>
export default {
  props: {
    to: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" src="./jbutton.scss"></style>
