<template>
  <section class="section">
    <div class="hero hero-text">
      <div class="columns is-centered">
        <div class="column has-text-centered purple">
          <h2 class="title">Web developer</h2>
          <p>A geek with a hat. Turning your idea to reality</p>
        </div>
        <div class="skills-container">
          <div class="skill-wrapper left">
            <div class="heading">Competences</div>
            <ul class="list">
              <li class="item">Creating & implementing exquisite interfaces</li>
              <li class="item">Finding the tools that are right for the job</li>
              <li class="item">Consulting about usability</li>
              <li class="item">User experience</li>
            </ul>
          </div>
          <div class="skill-wrapper middle">
            <div class="heading">Technologies</div>
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
          <div class="skill-wrapper right">
            <div class="heading">Process</div>
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
export default {}
</script>

<style lang="scss">
.hero-text {
  margin-top: 92px;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.purple {
  background-color: #ffdd00;
  width: 100vw;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  padding: 50px;
  padding-bottom: 100px;

  h2 {
    color: black;
  }
  p {
    color: black;
  }
}
.skills-container {
  width: 70%;
  margin: 0 auto;
  display: flex;
  margin-top: -50px;
  margin-bottom: 80px;
  -webkit-box-shadow: 0px 10px 26px 0px rgba(0, 0, 0, 0.16);
  -moz-box-shadow: 0px 10px 26px 0px rgba(0, 0, 0, 0.16);
  box-shadow: 0px 10px 26px 0px rgba(0, 0, 0, 0.16);
  .skill-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    width: 50%;
    border: 1px solid #e6ecf8;
    padding-bottom: 30px;
    .heading {
      font-size: 20px;
      margin-top: 20px;
      font-weight: 500;
    }
    .list {
      list-style: none;
      padding-left: 40px;
      width: 100%;
      .item {
        margin: 10px 0;
        &.last {
          text-align: center;
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
  }
}
.heading {
  text-align: center;
  font-size: 30px;
}
.divider {
  width: 100vw;
  background: #ffdd00;
  padding: 50px;
}
.elevator-container {
  display: flex;
  width: 100%;
  justify-content: center;
  background-color: white;
  margin-top: -20px;
}
</style>
