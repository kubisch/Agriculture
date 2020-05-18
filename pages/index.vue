<template>
  <div id="fullpage">
    <div class="container section">
      <div style="margin-top: 0 auto">
        <logo />
        <h1 class="title" style="animation: 6s fadein;">
          Agriculture
        </h1>
        <h2 class="subtitle" style="animation: 6.5s fadein;">
          Build a better world
        </h2>
        <hr style="animation: 7s fadein;" />
        <down-arrow />
      </div>
    </div>
    <div class="container section">
      <h1 class="title">
        Testing
      </h1>
      <h2 class="subtitle">
        Testing 2.0
      </h2>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import DownArrow from '~/components/DownArrow.vue'

export default {
  components: {
    Logo,
    DownArrow
  },
  mounted() {
    if (process.browser && window.$ !== undefined) {
      window.$(document).ready(function() {
        window.$('#fullpage').fullpage({ anchors: ['firstPage', 'secondPage'] })
      })
    }
  },
  head: {
    title: 'Agriculture',
    script: [
      {
        src: 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js'
      },
      {
        src:
          'https://cdnjs.cloudflare.com/ajax/libs/fullPage.js/2.9.7/jquery.fullpage.min.js'
      }
    ]
  }
}
</script>

<style>
@keyframes fadein {
  0% {
    opacity: 0;
  }
  75% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
  margin-bottom: 1rem;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

hr {
  margin-bottom: 25px;
}

.fp-section,
.fp-slide,
.fp-tableCell {
  height: auto !important;
}
</style>
