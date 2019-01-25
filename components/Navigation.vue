<template>
  <div class="navbar is-fluid">
    <div class="navbar-inner">
      <nuxt-link to="/">
        <img src="/images/logo.png">
      </nuxt-link>
      <div class="navbar-end">
        <nuxt-link to="/contact" class="navbar-item">Say hi</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  justify-content: center;
  .navbar-inner {
    width: 80%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    img {
      height: 100px;
      width: 100px;
    }
    .navbar-end {
      margin-right: 20px;
    }
  }
}
</style>
