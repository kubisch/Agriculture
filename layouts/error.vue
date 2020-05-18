<template>
  <div class="container">
    <div style="margin-top: 0 auto">
      <h1 class="title" style="animation: fadein 1.5s;">
        404: Page not found
      </h1>
      <h2 class="subtitle">
        <nuxt-link
          to="/"
          style="animation: fadein 2s; text-decoration: none; color: #35495e"
        >
          Go back?
        </nuxt-link>
      </h2>
    </div>
  </div>
</template>

<style>
@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
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
  margin-bottom: 2rem;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
</style>

<script>
export default {
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
