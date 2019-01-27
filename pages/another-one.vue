<template>
  <div class="container">
    <div class="hero center">
      <h1>Concept</h1>
      <p>Mobile application which shows various discounts on groceries in Denmark stores. Users are able to create their own shopping lists inside the application before going to store.</p>
    </div>
    <div class="hero">
      <div class="list">
        <div class="list-item">
          <img :src="`/images/another-one.png`">
        </div>
      </div>
    </div>
    <div class="hero dark">
      <h1>History</h1>
      <p>Application was started as a school project.</p>
    </div>
    <div class="hero light">
      <h1>Technologies used</h1>
      <div class="list">
        <div class="list-item tech">React Native</div>
        <div class="list-item tech">Redux</div>
        <div class="list-item tech">AWS</div>
        <div class="list-item tech">Node.js</div>
        <div class="list-item tech">Mongo DB</div>
        <div class="list-item tech">Laravel</div>
      </div>
    </div>
    <div class="cta">
      <a href="https://expo.io/@gintse/another-one">
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