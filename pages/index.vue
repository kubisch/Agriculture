<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        agriculture
      </h1>
      <h2 class="subtitle">
        You're a boomer
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/LogoDraw.vue'

export default {
  components: {
    Logo
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
  animation: 6.5s fadein;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  animation: 7s fadein;
}

.links {
  padding-top: 15px;
}
</style>
