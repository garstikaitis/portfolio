
<template>
  <div>
    <InnerNavigation link="https://cryptosandbox.eu"></InnerNavigation>
    <div class="container">
      <div class="hero center">
        <h1>Concept</h1>
        <p>
          We all, at some point in our lives wanted to cryptocurrency trading. But usually we are not feeling safe investing in something that we don't know.
          This is where
          <a
            href="https://cryptosandbox.eu"
          >CryptoSandbox</a> comes in.
          Users will start out with 10.000$ fictional capital and compete against other players in trading currencies which price is being calculated in real-time.
        </p>
      </div>
      <div class="hero">
        <div class="list">
          <div class="list-item" v-for="i in 2" :key="i">
            <img :src="`/images/cryptosandbox/${i}.png`">
          </div>
        </div>
      </div>
      <div class="hero dark">
        <h1>History</h1>
        <p>
          Project was started in
          <a target="_blank" href="https://nordichack.com/">NordicHack</a> hackathon and finished off later on.
        </p>
      </div>
      <div class="hero light">
        <h1>Technologies used</h1>
        <div class="list">
          <div class="list-item tech">Firebase</div>
          <div class="list-item tech">Vue.js</div>
          <div class="list-item tech">Netlify</div>
          <div class="list-item tech">SASS</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'inner',
  head() {
    return {
      title: 'Cryptocurrency trading sandbox | CryptoSandbox',
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          hid: 'description',
          name: 'description',
          content:
            'Web application which allows users to trade cryptocurrencies by using fictional money'
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
      img {
        max-width: 100vw;
      }
      .list-item {
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