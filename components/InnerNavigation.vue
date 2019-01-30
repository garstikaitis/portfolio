<template>
  <div class="nav-container">
    <a href="/">Go back</a>
    <a :href="link">Check it out</a>
  </div>
</template>

<script>
export default {
  props: ['link']
}
</script>

<style lang="scss" scoped>
.nav-container {
  background: black;
  display: flex;
  justify-content: space-around;
  padding: 30px;
  position: fixed;
  top: 0;
  width: 100%;
  a {
    border: 2px solid #89d1ff;
    background: #89d1ff;
    color: black;
    cursor: pointer;
    font-size: 15px;
    border-radius: 8px;
    padding: 15px;
    transition: all 0.2s ease-in;
    text-decoration: none;
    font-weight: 600;
    &:focus {
      outline: none;
    }
    &:active {
      outline: none;
    }
    &:hover {
      background-color: #89d1ff;
      color: black;
    }
  }
}
@media only screen and (max-width: 500px) {
  .nav-container {
    position: fixed;
    top: 0;
    display: flex;
    justify-content: space-around;
    width: 100%;
    background-color: black;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
    padding: 10px;
    a {
      border: 2px solid #ffdd55;
      background: transparent;
      color: #ffdd55;
      cursor: pointer;
      font-size: 15px;
      border-radius: 8px;
      padding: 15px;
      transition: all 0.2s ease-in;
      text-decoration: none;
      font-weight: 600;
      &:focus {
        outline: none;
      }
      &:active {
        outline: none;
      }
      &:hover {
        background-color: #ffdd55;
        color: black;
      }
    }
  }
}
</style>
