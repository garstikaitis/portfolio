<template>
  <div class="section">
    <div class="heading">Process</div>
    <div class="content-container">
      <div class="item" @click="changeStep(0)" :class="{active: step === 0}">
        <img class="icon" height="100" width="100" src="/images/process/constructivism.svg">
        <div class="title">Study current and potential customers to see what they need and want.</div>
      </div>
      <div class="item" @click="changeStep(1)" :class="{active: step === 1}">
        <img class="icon" height="100" width="100" src="/images/process/pencil.svg">
        <div class="title">Create functional requirements, flows, create clickable prototypes.</div>
      </div>
      <div class="item" @click="changeStep(2)" :class="{active: step === 2}">
        <img class="icon" height="100" width="100" src="/images/process/web.svg">
        <div class="title">Implement minimum viable product</div>
      </div>
      <div class="item" @click="changeStep(3)" :class="{active: step === 3}">
        <img class="icon" height="100" width="100" src="/images/process/analyze.svg">
        <div class="title">Give product for testing to target audience(s)</div>
      </div>
      <div class="item" @click="changeStep(4)" :class="{active: step === 4}">
        <img class="icon" height="100" width="100" src="/images/process/update.svg">
        <div
          class="title"
        >Refine current product version based on feedback gained from testing phase</div>
      </div>
    </div>
    <div class="illustration-container">
      <div class="timeline">
        <div class="step">
          <div @click="changeStep(0)" class="circle">
            <div v-if="step === 0" class="inner-circle"></div>
          </div>
          <div class="text">Hypothesis</div>
        </div>
        <div class="step">
          <div @click="changeStep(1)" class="circle">
            <div v-if="step === 1" class="inner-circle"></div>
          </div>
          <div class="text">Design</div>
        </div>
        <div class="step">
          <div @click="changeStep(2)" class="circle">
            <div v-if="step === 2" class="inner-circle"></div>
          </div>
          <div class="text">Code</div>
        </div>
        <div class="step">
          <div @click="changeStep(3)" class="circle">
            <div v-if="step === 3" class="inner-circle"></div>
          </div>
          <div class="text">Test</div>
        </div>
        <div class="step">
          <div @click="changeStep(4)" class="circle">
            <div v-if="step === 4" class="inner-circle"></div>
          </div>
          <div class="text">Adapt</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'How I work? | Process',
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          hid: 'description',
          name: 'description',
          content: 'Showcase of my working process'
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
      step: 0
    }
  },
  methods: {
    changeStep(step) {
      this.step = step
    }
  },
  mounted() {
    if (process.browser) {
      window.dispatchEvent(new Event('resize'))
    }
  }
}
</script>

<style lang="scss" scoped>
.section {
  height: 100vh;
  width: 100vw;
  background-color: #ffdc5f;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  .heading {
    margin-top: 50px;
    font-family: 'Slabo 27px';
    font-size: 40px;
  }
  .content-container {
    margin-top: 200px;
    display: flex;
    justify-content: space-around;
    width: 80%;
    .item {
      display: flex;
      flex-direction: column;
      align-items: center;
      opacity: 0.2;
      transition: all 0.5s ease-in;
      cursor: pointer;
      &.active {
        opacity: 1;
      }
      .icon {
        width: 100px;
        height: 100px;
      }
      .title {
        max-width: 200px;
        margin-top: 30px;
        font-size: 18px;
      }
    }
  }
  .illustration-container {
    width: 100%;
    height: 100%;
    .timeline {
      height: 10px;
      width: 80vw;
      position: absolute;
      left: 10vw;
      bottom: 20%;
      background-color: black;
      border-radius: 8px;
      display: flex;
      justify-content: space-around;
      .step {
        display: flex;
        justify-content: center;
        width: 20%;
        .circle {
          display: flex;
          align-items: center;
          justify-content: center;
          position: absolute;
          top: -10px;
          height: 30px;
          width: 30px;
          background-color: #ffdc5f;
          border: 2px solid black;
          border-radius: 50%;
          cursor: pointer;
          .inner-circle {
            height: 20px;
            width: 20px;
            background-color: black;
            border-radius: 50%;
          }
        }
        .text {
          margin-top: 30px;
          font-family: 'Slabo 27px';
          font-size: 22px;
        }
      }
    }
  }
}
</style>
