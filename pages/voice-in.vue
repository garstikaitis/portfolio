<template>
  <div>
    <InnerNavigation link="/"></InnerNavigation>
    <div class="container">
      <div class="hero center">
        <h1>Concept</h1>
        <p>Probably everyone knows application Tinder. Instead of people liking pictures, VoiceIN were using diferent strategy - showcasing people voices. After a match was present, people pictures would appear.</p>
      </div>
      <div class="hero">
        <div class="list">
          <div class="list-item">
            <img :src="`/images/voice-in.jpg`">
          </div>
        </div>
      </div>
      <div class="hero dark">
        <h1>History</h1>
        <p>
          Project was started in
          <a
            target="_blank"
            href="http://communities.techstars.com/denmark/aalborg/startup-weekend/"
          >Startup Weekend Aalborg</a>
        </p>
      </div>
      <div class="hero light">
        <h1>Technologies used</h1>
        <div class="list">
          <div class="list-item tech">Swift</div>
          <div class="list-item tech">Firebase</div>
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
      title: 'Dating application | Voice IN',
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          hid: 'description',
          name: 'description',
          content:
            'Application which allows people to meet by using only their voices.'
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
