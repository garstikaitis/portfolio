<template>
  <div class="navbar is-fluid">
    <div class="navbar-inner">
      <a href="/">
        <img src="/images/logo.png">
      </a>
      <div class="navbar-end">
        <button @click="writeMail()" to="/contact" class="navbar-item">Let's get in touch</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    writeMail() {
      var mail = document.createElement('a')
      mail.href = 'mailto:hi@gintaras.tech'
      mail.click()
    }
  }
}
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
      button {
        border: 2px solid black;
        padding: 20px;
        border-radius: 8px;
        color: black;
        text-decoration: none;
        font-weight: 500;
        background-color: transparent;
        cursor: pointer;
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
@media only screen and (max-width: 500px) {
  .navbar {
    .navbar-inner {
      justify-content: center;
      .navbar-end {
        display: none;
      }
    }
  }
}
</style>
