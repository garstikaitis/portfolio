<template>
  <div class="container">
    <div class="hero center">
      <h1>Concept</h1>
      <p>Talenthub is a platform which helps recruites to analyze their candidate experience.</p>
    </div>
    <div class="hero">
      <div class="list">
        <div class="list-item" v-for="i in 5" :key="i">
          <img :src="`/images/talenthub/${i}.png`">
        </div>
      </div>
    </div>
    <div class="hero dark">
      <h1>History</h1>
      <p>Project was started in back when I was working at Talenthub</p>
    </div>
    <div class="hero light">
      <h1>Technologies used</h1>
      <div class="list">
        <div class="list-item tech">Storyblok CMS</div>
        <div class="list-item tech">Nuxt.js</div>
        <div class="list-item tech">Vuex</div>
        <div class="list-item tech">AWS</div>
        <div class="list-item tech">SASS</div>
      </div>
    </div>
    <div class="cta">
      <a href="https://talenthub.io">
        <button>Check it out</button>
      </a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.container {
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    width: 100vw;
    h1 {
      font-family: 'Slabo 27px', serif;
      font-size: 42px;
      margin-bottom: 20px;
    }
    p {
      font-size: 22px;
      max-width: 400px;
      text-align: center;
      line-height: 30px;
    }
    &.dark {
      background-color: #ffb355;
    }
    &.center {
      background-color: #ffdc5f;
    }
    &.light {
      background-color: #ffdd55;
    }
    .list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      .list-item {
        img {
          max-width: 100vw;
        }
        &.tech {
          padding: 10px;
          font-size: 22px;
        }
      }
    }
  }
  .cta {
    width: 100vw;
    background-color: black;
    padding: 50px;
    display: flex;
    justify-content: center;
    a {
      button {
        border: 2px solid #ffdd55;
        background: transparent;
        color: #ffdd55;
        cursor: pointer;
        font-size: 20px;
        border-radius: 8px;
        padding: 20px;
        transition: all 0.2s ease-in;
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
  .title {
    text-align: center;
  }
}
</style>
