<template>
  <div style="position: relative; min-height: 100vh;">
    <navbar />
    <div style="margin-top: -5.5rem">
      <div class="container section">
        <div style="margin-top: 0 auto">
          <LogoNoAnim />
          <h1 class="title">
            Agriculture
          </h1>
          <h2 class="subtitle">
            Build a better world
          </h2>
          <hr />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import LogoNoAnim from '~/components/LogoNoAnim.vue'
// import DownArrow from '~/components/DownArrow.vue'

export default {
  components: {
    Navbar,
    LogoNoAnim //,
    // DownArrow
  },
  mounted() {
    // if (process.browser && window.$ !== undefined) {
    //   window.$(document).ready(function() {
    //     window.$('#fullpage').fullpage({ anchors: ['firstPage', 'secondPage'] })
    //   })
    // }
  },
  head: {
    title: 'Agriculture' //,
    /* script: [
      {
        src: 'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js'
      },
      {
        src:
          'https://cdnjs.cloudflare.com/ajax/libs/fullPage.js/2.9.7/jquery.fullpage.min.js'
      }
    ] */
  }
}
</script>

<style scoped lang="scss">
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

$t-duration: 600ms;
$t-delay: 150ms;

.page-enter-active,
.page-leave-active {
  transition-duration: $t-duration * 2;

  &::before,
  &::after {
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    z-index: 2;
    display: block;
    width: 100%;
    height: 50%;
    transition-property: opacity, transform;
    transition-timing-function: ease-in-out;
  }

  &::before {
    background-color: #2e2e2e;
  }

  &::after {
    top: 50%;
    background-color: #2e2e2e;
  }
}

.page-leave {
  &::before,
  &::after {
    transform: scaleX(0);
  }
}

.page-leave-active {
  &::before {
    transition-duration: $t-duration;
  }

  &::after {
    transition-duration: $t-duration - $t-delay;
    transition-delay: $t-delay;
  }
}

.page-leave-to {
  &::before,
  &::after {
    transform: scale(1);
    transform-origin: left;
  }
}

.page-enter {
  &::before,
  &::after {
    transform: scaleX(1);
  }
}

.page-enter-active {
  &::before {
    transition-duration: $t-duration;
  }

  &::after {
    transition-duration: $t-duration - $t-delay;
    transition-delay: $t-delay;
  }
}

.page-enter-to {
  &::before,
  &::after {
    transform: scaleX(0);
    transform-origin: right;
  }
}
</style>
