<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <nuxt-link class="navbar-brand" to="/home">
      <svg
        width="48"
        height="40"
        viewBox="0 0 60 50"
        xmlns="http://www.w3.org/2000/svg"
        style="padding-top: 5px; padding-bottom: 0px"
      >
        <g fill-rule="evenodd" transform="scale(0.125)">
          <path
            d="M139 330l-1-2c-2-4-2-8-1-13H29L189 31l67 121 22-16-67-121c-1-2-9-14-22-14-6 0-15 2-22 15L5 303c-1 3-8 16-2 27 4 6 10 12 24 12h136c-14 0-21-6-24-12z"
            stroke="#00C58E"
            stroke-width="4"
            fill="rgba(0,197,142,1)"
          />
          <path
            d="M447 304L317 70c-2-2-9-15-22-15-6 0-15 3-22 15l-17 28v54l39-67 129 230h-49a23 23 0 0 1-2 14l-1 1c-6 11-21 12-23 12h76c3 0 17-1 24-12 3-5 5-14-2-26z"
            stroke="#108775"
            stroke-width="4"
            fill="rgba(16,135,117,1)"
          />
          <path
            d="M376 330v-1l1-2c1-4 2-8 1-12l-4-12-102-178-15-27h-1l-15 27-102 178-4 12a24 24 0 0 0 2 15c4 6 10 12 24 12h190c3 0 18-1 25-12zM256 152l93 163H163l93-163z"
            stroke="#2F495E"
            stroke-width="4"
            fill="rgba(47,73,94,1)"
          />
        </g>
      </svg>
      <div style="float: right; margin-top: 6px; margin-left: 4px;">
        Agriculture
      </div>
    </nuxt-link>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNavAltMarkup"
      aria-controls="navbarNavAltMarkup"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div id="navbarNavAltMarkup" class="collapse navbar-collapse">
      <div class="navbar-nav">
        <a class="nav-item nav-link" href="#">The Issues</a>
        <nuxt-link to="/contact" class="nav-item nav-link"
          >Contact Us</nuxt-link
        >
        <nuxt-link to="/donate" class="nav-item nav-link">Donate</nuxt-link>
      </div>
    </div>
  </nav>
</template>

<style>
nav {
  position: absolute;
  /* z-index: 99; */
}

@media (min-width: 992px) {
  nav {
    z-index: 99;
  }
}

.navbar {
  padding-left: 10%;
}

.navbar-nav {
  margin-top: 4px;
}

#navbarNavAltMarkup {
  padding-right: 10%;
}
</style>
