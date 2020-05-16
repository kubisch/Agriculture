<template>
  <svg
    class="Logo"
    width="245"
    height="180"
    viewBox="0 0 452 342"
    xmlns="http://www.w3.org/2000/svg"
  >
    <g fill="none" fill-rule="evenodd">
      <path
        id="LogoPath1"
        d="M139 330l-1-2c-2-4-2-8-1-13H29L189 31l67 121 22-16-67-121c-1-2-9-14-22-14-6 0-15 2-22 15L5 303c-1 3-8 16-2 27 4 6 10 12 24 12h136c-14 0-21-6-24-12z"
        stroke="#00C58E"
        stroke-width="4"
        fill="none"
      />
      <path
        id="LogoPath2"
        d="M447 304L317 70c-2-2-9-15-22-15-6 0-15 3-22 15l-17 28v54l39-67 129 230h-49a23 23 0 0 1-2 14l-1 1c-6 11-21 12-23 12h76c3 0 17-1 24-12 3-5 5-14-2-26z"
        stroke="#108775"
        stroke-width="4"
        fill="none"
      />
      <path
        id="LogoPath3"
        d="M376 330v-1l1-2c1-4 2-8 1-12l-4-12-102-178-15-27h-1l-15 27-102 178-4 12a24 24 0 0 0 2 15c4 6 10 12 24 12h190c3 0 18-1 25-12zM256 152l93 163H163l93-163z"
        stroke="#2F495E"
        stroke-width="4"
        fill="none"
      />
    </g>
  </svg>
</template>

<style>
.Logo {
  margin: auto;
  margin-top: 50px;
  opacity: 0;
}
</style>

<script>
import anime from 'animejs/lib/anime.es.js'

export default {
  mounted() {
    document.getElementsByClassName('Logo')[0].style.opacity = 1
    const tl = anime.timeline()
    tl.add({
      targets: '#LogoPath3',
      strokeDashoffset: [anime.setDashoffset, 0],
      easing: 'easeInOutQuad',
      duration: 3000,
      delay: 500
    })
      .add(
        {
          targets: '#LogoPath3',
          fill: '#2F495E',
          easing: 'easeInOutSine',
          duration: 1000
        },
        '-=1250'
      )
      .add(
        {
          targets: '#LogoPath1',
          strokeDashoffset: [anime.setDashoffset, 0],
          easing: 'easeInOutSine',
          direction: 'alternate',
          duration: 1500
        },
        '-=1000'
      )
      .add(
        {
          targets: '#LogoPath2',
          strokeDashoffset: [anime.setDashoffset, 0],
          easing: 'easeInOutSine',
          direction: 'alternate',
          duration: 1500
        },
        '-=1000'
      )
      .add(
        {
          targets: '#LogoPath1',
          fill: '#00C58E',
          easing: 'easeInOutQuad',
          duration: 1000
        },
        '-=600'
      )
      .add(
        {
          targets: '#LogoPath2',
          fill: '#108775',
          easing: 'easeInOutQuad',
          duration: 1000
        },
        '-=400'
      )
  }
}
</script>
