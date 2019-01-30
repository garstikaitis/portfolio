<template>
  <section class="section">
    <div class="hero hero-text">
      <div class="columns is-centered">
        <div class="column has-text-centered purple">
          <h2 class="title">Full stack developer</h2>
          <p>A geek with a hat 🧢 Turning your idea to reality</p>
          <img src="/images/hero.jpg">
          <div class="tabs">
            <div
              class="tab"
              @click="tabActive = 'competences'"
              :class="{ active: tabActive === 'competences' }"
            >Competences</div>
            <div
              class="tab"
              @click="tabActive = 'technologies'"
              :class="{ active: tabActive === 'technologies' }"
            >Technologies</div>
            <div
              class="tab"
              @click="tabActive = 'process'"
              :class="{ active: tabActive === 'process' }"
            >Process</div>
          </div>
          <div class="skills-container">
            <div class="skill-wrapper" v-show="tabActive === 'competences'">
              <ul class="list">
                <li class="item">Creating & implementing exquisite interfaces</li>
                <li class="item">Finding the tools that are right for the job</li>
                <li class="item">Proposing solutions built from scratched</li>
                <li class="item">Consulting about usability</li>
                <li class="item">Nerding about user experience</li>
              </ul>
            </div>
            <div class="skill-wrapper" v-show="tabActive === 'technologies'">
              <ul class="list">
                <li class="item">React</li>
                <li class="item">Vue.js</li>
                <li class="item">React Native</li>
                <li class="item">Laravel</li>
                <li class="item">Node.js</li>
                <li class="item">Amazon Web Services</li>
                <li class="item">Docker</li>
                <li class="item">SASS</li>
              </ul>
            </div>
            <div class="skill-wrapper" v-show="tabActive === 'process'">
              <ul class="list">
                <li class="item">Analyzing business requirements</li>
                <li class="item">Coming up with content requirements</li>
                <li class="item">Creating functional requirements</li>
                <li class="item">Working within agile framework</li>
                <li class="item">Iterating</li>
                <li class="item last">
                  <button @click="navigate">See example</button>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <section class="section mobile">
      <div class="heading">Recent works</div>
      <Grid/>
    </section>
    <section class="section">
      <div class="divider">
        <div class="heading">Liked what you saw?</div>
        <div class="cta">
          <button @click="writeMail()" class="button">Let's get in touch!</button>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
export default {
  head() {
    return {
      title: 'Gintaras Arstikaitis | Portfolio',
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          hid: 'description',
          name: 'description',
          content: 'Full stack developer with 2+ years of experience'
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
  },
  data() {
    return {
      tabActive: 'competences'
    }
  },
  methods: {
    writeMail() {
      var mail = document.createElement('a')
      mail.href = 'mailto:hi@gintaras.tech'
      mail.click()
    },
    navigate() {
      window.location.href = '/process'
    }
  }
}
</script>

<style lang="scss">
@keyframes driveInTitle {
  from {
    transform: translate(-200px);
    opacity: 0;
  }
  to {
    transform: translate(0px);
    opacity: 1;
  }
}
.hero-text {
  width: 85%;
  margin: 0 auto;
}
.title {
  font-family: 'Slabo 27px', serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.purple {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 50px;
  padding-bottom: 100px;
  min-height: 1000px;
  margin-top: 120px;
  .tabs {
    display: flex;
    width: 50%;
    margin-top: 20px;
    animation: driveInTitle 1s cubic-bezier(0.57, 0.21, 0.69, 1.25);
    .tab {
      padding: 20px;
      border: 2px solid black;
      margin-right: 10px;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.2s ease-in;
      &:hover {
        background: black;
        color: #ffdc5f;
      }
      &.active {
        background: black;
        color: #ffdc5f;
      }
    }
  }
  img {
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1;
    width: 100%;
  }
  h2 {
    color: black;
    animation: driveInTitle 0.8s cubic-bezier(0.57, 0.21, 0.69, 1.25);
  }
  p {
    color: black;
    animation: driveInTitle 0.9s cubic-bezier(0.57, 0.21, 0.69, 1.25);
  }
}
.skills-container {
  width: 50%;
  display: flex;
  flex-direction: column;
  margin-top: 30px;
  margin-bottom: 80px;
  .skill-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    padding-bottom: 30px;
    animation: driveInTitle 0.5s cubic-bezier(0.57, 0.21, 0.69, 1.25);
    .list {
      list-style: none;
      width: 100%;
      padding-left: 0;
      .item {
        margin: 10px 0;
        font-family: 'Slabo 27px';
        font-size: 27px;
        &.last {
          button {
            border: 2px solid black;
            background: transparent;
            padding: 20px;
            border-radius: 8px;
            color: black;
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: all 0.2s ease-in;
            cursor: pointer;
            &:hover {
              background-color: black;
              color: #ffdc5f;
            }
            &:active {
              outline: none;
            }
            &:focus {
              outline: none;
            }
          }
        }
      }
    }
    &.left {
      border-top-left-radius: 8px;
      border-bottom-left-radius: 8px;
      border-right: none;
    }
    &.right {
      border-top-right-radius: 8px;
      border-bottom-right-radius: 8px;
    }
    &.bottom {
      width: 100%;
    }
  }
}
.heading {
  text-align: center;
  font-size: 30px;
  font-family: 'Slabo 27px', serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  margin-bottom: 50px;
  color: black;
}
.divider {
  width: 100vw;
  background: #ffdc5f;
  padding: 50px;
  .cta {
    text-align: center;
    button {
      border: 2px solid black;
      padding: 20px;
      border-radius: 8px;
      color: black;
      background: #ffdd00;
      text-decoration: none;
      font-weight: 500;
      font-size: 16px;
      transition: all 0.2s ease-in;
      cursor: pointer;
      &:hover {
        background-color: black;
        color: white;
      }
    }
  }
}
@media only screen and (max-width: 500px) {
  .hero-text {
    width: 100%;
    margin: 0 auto;
  }
  .purple {
    margin-top: initial;
    position: relative;
    overflow: hidden;
    p {
    }
    h2 {
      font-size: 30px;
    }
    img {
      height: initial;
      width: initial;
    }
    .tabs {
      flex-direction: column;
      width: initial;
      .tab {
        margin: 10px 0;
      }
    }
  }
  .skills-container {
    width: initial;
  }
  .mobile {
    margin-top: -65px;
  }
}
</style>
