<template>
  <div class="grid">
    <div class="grid-item">
      <div class="content">
        <img :src="require('../static/images/widget.png')" @mouseenter="handleHover(4)">
        <nuxt-link
          to="/widget"
          class="overlay"
          style="background-color: rgba(53, 5, 235, 0.9);"
          @mouseleave="handleHover(null)"
          v-if="showOverlayIndex === 4"
        >
          <div class="name">Embeddable widget</div>
          <div class="description">Embeddable widget for collecting data from users</div>
          <button class="cta">
            Read more
            <img src="/images/read-more-white.png">
          </button>
        </nuxt-link>
      </div>
    </div>
    <div class="grid-item">
      <div class="content">
        <img :src="require('../static/images/cryptosandbox.png')" @mouseenter="handleHover(0)">
        <nuxt-link
          class="overlay"
          to="/cryptosandbox"
          style="background-color: rgba(63, 223, 255, 0.9);"
          @mouseleave="handleHover(null)"
          v-if="showOverlayIndex === 0"
        >
          <div class="name">CRYPTOSANDBOX</div>
          <div class="description">Cryptocurrent trading sandbox</div>
          <button class="cta">
            Read more
            <img src="/images/read-more-white.png">
          </button>
        </nuxt-link>
      </div>
    </div>
    <div class="grid-item">
      <div class="content">
        <img :src="require('../static/images/talenthub.png')" @mouseenter="handleHover(3)">
        <nuxt-link
          to="/talenthub"
          class="overlay"
          style="background-color: rgba(38, 191, 127, 0.9);"
          @mouseleave="handleHover(null)"
          v-if="showOverlayIndex === 3"
        >
          <div class="name">Talenthub.io</div>
          <div class="description">Landing page for a startup</div>
          <button class="cta">
            Read more
            <img src="/images/read-more-white.png">
          </button>
        </nuxt-link>
      </div>
    </div>
    <div class="grid-item">
      <div class="content">
        <img :src="require('../static/images/interhelps.png')" @mouseenter="handleHover(1)">
        <nuxt-link
          to="/interhelps"
          class="overlay"
          style="background-color: rgba(247, 63, 82, 0.9);"
          @mouseleave="handleHover(null)"
          v-if="showOverlayIndex === 1"
        >
          <div class="name">Interhelps</div>
          <div class="description">Representational website for event</div>
          <button class="cta">
            Read more
            <img src="/images/read-more-white.png">
          </button>
        </nuxt-link>
      </div>
    </div>
    <div class="grid-item">
      <div class="content">
        <img :src="require('../static/images/GOTWiki.png')" @mouseenter="handleHover(2)">
        <nuxt-link
          style="background-color: rgba(255, 254, 184, 0.9);"
          to="/gotwiki"
          class="overlay"
          @mouseleave="handleHover(null)"
          v-if="showOverlayIndex === 2"
        >
          <div style="color: black;" class="name">GAME OF THRONES WIKI</div>
          <div
            style="color: black;"
            class="description"
          >Encyclopedia app for game of thrones TV show</div>
          <button style="color: black; border: 1px solid black;" class="cta">
            Read more
            <img src="/images/read-more.png">
          </button>
        </nuxt-link>
      </div>
    </div>
    <div class="grid-item">
      <div class="content">
        <img :src="require('../static/images/voice-in.jpg')" @mouseenter="handleHover(5)">
        <nuxt-link
          to="/voice-in"
          class="overlay"
          style="background-color: rgba(227, 57, 102, 0.9);"
          @mouseleave="handleHover(null)"
          v-if="showOverlayIndex === 5"
        >
          <div class="name">VoiceIN</div>
          <div class="description">Dating application</div>
          <button class="cta">
            Read more
            <img src="/images/read-more-white.png">
          </button>
        </nuxt-link>
      </div>
    </div>
    <div class="grid-item">
      <div class="content">
        <img :src="require('../static/images/another-one.png')" @mouseenter="handleHover(6)">
        <nuxt-link
          to="/another-one"
          class="overlay"
          style="background-color: rgba(20, 4, 64, 0.9);"
          @mouseleave="handleHover(null)"
          v-if="showOverlayIndex === 6"
        >
          <div class="name">Another One</div>
          <div class="description">Grocery discount application</div>
          <button class="cta">
            Read more
            <img src="/images/read-more-white.png">
          </button>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
const imagesLoaded = require('imagesloaded')
export default {
  data() {
    return {
      showOverlayIndex: null
    }
  },
  methods: {
    handleHover(index) {
      this.showOverlayIndex = index
    },
    resizeGridItem(item) {
      const grid = document.getElementsByClassName('grid')[0]
      const rowHeight = parseInt(
        window.getComputedStyle(grid).getPropertyValue('grid-auto-rows')
      )
      const rowGap = parseInt(
        window.getComputedStyle(grid).getPropertyValue('grid-row-gap')
      )
      const rowSpan = Math.ceil(
        (item.querySelector('.content').getBoundingClientRect().height +
          rowGap) /
          (rowHeight + rowGap)
      )
      item.style.gridRowEnd = 'span ' + rowSpan
    },
    resizeAllGridItems() {
      let allItems = document.getElementsByClassName('grid-item')
      for (let x = 0; x < allItems.length; x++) {
        imagesLoaded(allItems[x], this.resizeInstance)
      }
    },
    resizeInstance(instance) {
      const item = instance.elements[0]
      this.resizeGridItem(item)
    }
  },
  mounted() {
    if (process.browser) {
      window.dispatchEvent(new Event('resize'))
      window.addEventListener('resize', this.resizeAllGridItems)
      window.onNuxtReady(app => {
        imagesLoaded('.grid', () => {
          window.dispatchEvent(new Event('resize'))
          this.resizeAllGridItems()
          window.addEventListener('resize', this.resizeAllGridItems)
        })
      })
    }
  }
}
</script>

<style lang="scss" scoped>
@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
.grid {
  display: grid;
  grid-gap: 10px;
  grid-template-columns: repeat(auto-fill, minmax(500px, 1fr));
  grid-auto-rows: 20px;
  width: 80%;
  margin: 0 auto;
}
.grid-sizer {
  width: 50%;
}
.grid-item {
  .content {
    position: relative;
    text-align: center;
    img {
      height: auto;
      max-width: 100%;
    }
    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      animation: fadein 1s;
      .name {
        font-size: 30px;
        color: white;
      }
      .description {
        font-size: 15px;
        color: white;
      }
      .cta {
        background-color: transparent;
        width: 50%;
        padding: 10px;
        color: white;
        border: none;
        border: 2px solid white;
        outline: none;
        cursor: pointer;
        font-size: 20px;
        margin-top: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        &:active {
          outline: none;
        }
        &:hover {
          img {
            margin-left: 20px;
            transition: all 0.2s ease-in;
            transform: scaleX(1.5) translateX(20px);
          }
        }
        img {
          margin-left: 20px;
          transition: all 0.2s ease-in;
        }
      }
    }
  }
}
@media only screen and (max-width: 500px) {
  .grid {
    grid-template-columns: repeat(auto-fill, minmax(100%, 1fr));
    .grid-item {
      .content {
        .overlay {
          .name {
            font-size: 22px;
            margin-bottom: 10px;
          }
          .description {
            text-align: center;
          }
        }
      }
    }
  }
}
</style>
