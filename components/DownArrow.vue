<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 96 150" width="96px">
    <g transform="scale(0.375)">
      <path
        class="cls-1"
        d="M128,220.24H128L63.2,143a5.59,5.59,0,0,1,0-6.92,3.66,3.66,0,0,1,5.8,0l54.69,65.18s.07,0,.07,0v-162a3.28,3.28,0,0,1,3-3.53h2.56a3.29,3.29,0,0,1,3,3.53v162s0,.07.07,0l54.52-65a3.8,3.8,0,0,1,6.11,0,5.6,5.6,0,0,1-.14,6.74Z"
        stroke="#2F495E"
        stroke-width="4"
        fill="none"
      />
    </g>
  </svg>
</template>

<style>
.cls-1 {
  stroke-linecap: round;
  stroke-linejoin: round;
  opacity: 0;
}
</style>

<script>
import anime from 'animejs/lib/anime.es.js'

export default {
  mounted() {
    document.getElementsByClassName('cls-1')[0].style.opacity = 1
    const tl = anime.timeline()
    tl.add({
      targets: '.cls-1',
      strokeDashoffset: [anime.setDashoffset, 0],
      easing: 'easeInOutQuad',
      duration: 1200,
      delay: 7000
    })
      .add(
        {
          targets: '.cls-1',
          fill: '#2F495E',
          easing: 'easeInOutSine',
          duration: 400
        },
        '-=400'
      )
      .add({
        targets: '.cls-1',
        keyframes: [
          { translateY: -25 },
          { translateY: 50 },
          { translateY: -25 },
          { translateY: 50 },
          { translateY: -25 },
          { translateY: 50 }
        ],
        easing: 'easeInOutSine',
        duration: 6000,
        direction: 'alternate',
        loop: true
      })
  }
}
</script>
