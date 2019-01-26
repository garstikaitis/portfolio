<template>
  <section class="section">
    <div class="hero hero-text">
      <div class="columns is-centered">
        <div class="column has-text-centered purple">
          <h2 class="title">Web developer</h2>
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
            <div class="skill-wrapper" v-if="tabActive === 'competences'">
              <ul class="list">
                <li class="item">Creating & implementing exquisite interfaces</li>
                <li class="item">Finding the tools that are right for the job</li>
                <li class="item">Consulting about usability</li>
                <li class="item">User experience</li>
              </ul>
            </div>
            <div class="skill-wrapper" v-else-if="tabActive === 'technologies'">
              <ul class="list">
                <li class="item">React</li>
                <li class="item">Vue.js</li>
                <li class="item">Laravel</li>
                <li class="item">Node.js</li>
                <li class="item">Amazon Web Services</li>
                <li class="item">Docker</li>
                <li class="item">SASS</li>
                <li class="item">BEM</li>
              </ul>
            </div>
            <div class="skill-wrapper" v-else-if="tabActive === 'process'">
              <ul class="list">
                <li class="item">Analyzing business requirements</li>
                <li class="item">Coming up with content requirements</li>
                <li class="item">Creating functional requirements</li>
                <li class="item">Working within agile framework</li>
                <li class="item">Iterating</li>
                <li class="item last">
                  <button>See example</button>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <section class="section">
      <div class="heading">Recent works</div>
      <Grid/>
    </section>
    <section class="section">
      <div class="divider">
        <div class="heading">Liked what you saw?</div>
      </div>
    </section>
    <div class="elevator-container">
      Let's get in
      <button class="button">touch!</button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      tabActive: 'competences'
    }
  }
}
</script>

<style lang="scss">
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
  width: 100vw;
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
    .tab {
      padding: 20px;
      border: 2px solid black;
      margin-right: 10px;
      border-radius: 8px;
      cursor: pointer;
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
  }
  p {
    color: black;
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

    .list {
      list-style: none;
      width: 100%;
      padding-left: 0;
      .item {
        margin: 10px 0;
        font-family: 'Slabo 27px';
        font-size: 27px;
        &.last {
          text-align: center;
          button {
            border: 2px solid #ffdd00;
            padding: 20px;
            border-radius: 8px;
            color: black;
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: all 0.2s ease-in;
            cursor: pointer;
            &:hover {
              background-color: #ffdd00;
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
  color: #35495e;
}
.divider {
  width: 100vw;
  background: #ffdd00;
  padding: 50px;
}
.elevator-container {
  display: flex;
  width: 50%;
  justify-content: center;
  background-color: white;
  margin: 0 auto;
  margin-top: -20px;
  margin-bottom: 50px;
  /* margin: 0 auto; */
  border-radius: 8px;
  padding: 30px;
  border: 1px solid #e8e8e8;
  box-shadow: 0px 10px 26px 0px rgba(0, 0, 0, 0.16);
}
</style>
