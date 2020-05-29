<template>
  <div style="position: relative; min-height: 100vh;">
    <div class="navAnim">
      <navbar />
    </div>
    <div style="margin-top: -5.5rem">
      <div class="container section">
        <div style="margin-top: 0 auto">
          <logo />
          <h1 class="title">
            Agriculture
          </h1>
          <h2 class="subtitle">
            Build a better world
          </h2>
          <hr />
          <!-- <down-arrow /> -->
        </div>
      </div>
      <!-- <div class="container section">
        <h1 class="title">
          Testing
        </h1>
        <h2 class="subtitle">
          Testing 2.0
        </h2>
      </div> -->
    </div>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import Logo from '~/components/Logo.vue'
// import DownArrow from '~/components/DownArrow.vue'

export default {
  components: {
    Navbar,
    Logo //,
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
@keyframes fadein {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes navbarFadein {
  0% {
    opacity: 0;
    transform: translateY(-2rem);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.navAnim {
  opacity: 0;
  animation-name: navbarFadein;
  animation-duration: 4s;
  animation-delay: 3.5s;
  animation-fill-mode: forwards;
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
  opacity: 0;
  animation-name: fadein;
  animation-duration: 1.5s;
  animation-delay: 4.5s;
  animation-fill-mode: forwards;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  opacity: 0;
  animation-name: fadein;
  animation-duration: 1.625s;
  animation-delay: 4.875s;
  animation-fill-mode: forwards;
}

hr {
  margin-bottom: 25px;
  opacity: 0;
  animation-name: fadein;
  animation-duration: 1.75s;
  animation-delay: 5.25s;
  animation-fill-mode: forwards;
}

@media (max-width: 482px) {
  .title {
    font-family: 'Quicksand', 'Source Sans Pro', -apple-system,
      BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial,
      sans-serif;
    display: block;
    font-weight: 300;
    font-size: 60px;
    color: #35495e;
    letter-spacing: 1px;
    margin-bottom: 0.6rem;
  }

  .subtitle {
    font-weight: 300;
    font-size: 25.2px;
    color: #526488;
    word-spacing: 3px;
    padding-bottom: 10px;
  }

  hr {
    margin-bottom: 25px;
  }
}

$t-duration: 600ms;
$t-delay: 150ms;

.page-leave-active {
  transition-duration: $t-duration * 2;

  &::before,
  &::after {
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    z-index: 0;
    display: block;
    width: 100%;
    height: 50%;
    transition-property: opacity, transform;
    transition-timing-function: ease-in-out;
  }
  @media (max-width: 991px) {
    &::before,
    &::after {
      z-index: 2;
    }
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
</style>
