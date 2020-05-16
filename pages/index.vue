<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        agriculture
      </h1>
      <h2 class="subtitle">
        Hope for a better world
      </h2>
      <hr />
      <down-arrow />
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

hr {
  animation: 7.5s fadein;
  margin-bottom: 25px;
}
</style>
