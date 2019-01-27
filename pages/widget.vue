<template>
  <div class="container">
    <div class="hero center">
      <h1>Concept</h1>
      <p>Widget which clients could embed to their career sites and ask various questions regarding their candidates recruitment experience.</p>
    </div>
    <div class="hero">
      <div class="list">
        <div class="list-item" v-for="i in 5" :key="i">
          <img :src="`/images/widget/${i}.png`">
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
        <div class="list-item tech">Laravel</div>
        <div class="list-item tech">Vue.js</div>
        <div class="list-item tech">Vuex</div>
        <div class="list-item tech">AWS</div>
        <div class="list-item tech">SASS</div>
      </div>
    </div>
    <div class="cta">
      <a href="https://s3.eu-central-1.amazonaws.com/th-widget-test/index.html">
        <button>Check it out</button>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Embeddable widget | Talenthub',
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          hid: 'description',
          name: 'description',
          content:
            'Widget which can be embedded to career sites and start tracking your candidates recruitment experience'
        }
      ],
      link: [
        { rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' },
        {
          rel: 'stylesheet',
          href:
            'https://fonts.googleapis.com/css?family=Asap|Quattrocento|Slabo+27px'
        }
      ]
    }
  }
}
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
