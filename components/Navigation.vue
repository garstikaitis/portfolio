<template>
  <div class="navbar is-fluid">
    <div class="navbar-inner">
      <nuxt-link to="/">
        <img src="/images/logo.png">
      </nuxt-link>
      <div class="navbar-end">
        <nuxt-link to="/contact" class="navbar-item">Let's get in touch</nuxt-link>
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
      a {
        border: 2px solid black;
        padding: 20px;
        border-radius: 8px;
        color: black;
        text-decoration: none;
        font-weight: 500;
        font-size: 16px;
        transition: all 0.2s ease-in;
        &:hover {
          background-color: black;
          color: white;
        }
      }
    }
  }
}
</style>
