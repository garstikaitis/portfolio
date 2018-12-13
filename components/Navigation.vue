<template>
  <div class="navbar is-fluid">
    <nuxt-link to="/">
      <img src="/images/logo.png">
    </nuxt-link>
    <div class="navbar-end">
      <nuxt-link to="/" class="navbar-item">Projects</nuxt-link>
      <nuxt-link to="/about" class="navbar-item">About</nuxt-link>
      <nuxt-link to="/contact" class="navbar-item">Contact</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
img {
  height: 100px;
  width: 100px;
}
</style>
