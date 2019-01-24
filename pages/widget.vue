<template>
  <div class="container">
    <div class="image">
      <img src="/images/widget.png">
    </div>
    <div class="content">
      <h1>History</h1>
      <p>Project was started in back when I was working at Talenthub</p>
      <h1>Concept</h1>
      <p>I was asked to build a widget which clients could embed to their career sites and ask various questions regarding their candidates recruitment experience.</p>
      <h1>Technologies used</h1>
      <ul>
        <li>Vue.js</li>
        <li>Vuex</li>
        <li>AWS</li>
        <li>SASS</li>
        <li>Laravel</li>
      </ul>
      <a href="https://s3.eu-central-1.amazonaws.com/th-widget-test/index.html">
        <button>Visit</button>
      </a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.container {
  .title {
    text-align: center;
  }
}
</style>
