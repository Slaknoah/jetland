<template>
  <header class="header">
    <div class="container">
      <a class="header__logo" to="/">
        <logo></logo>
      </a>

      <Menu />
    </div>
  </header>
</template>

<script>
import Logo from '~/components/logos/Logo';
export default {
  components: {
    Logo
  }
}
</script>

<style lang="scss" src="./header.scss"></style>