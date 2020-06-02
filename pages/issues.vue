<template>
  <div style="position: relative; min-height: 100vh;">
    <navbar />
    <div class="container main-content" style="padding-bottom: 4rem;">
      <div class="row justify-content-between" style="margin-top: 2rem">
        <h5 class="title">The issues</h5>
        <hr style="margin-bottom: 5rem;" />
        <div class="container">
          <div class="row">
            <div class="col-7">
              In a recent survey that we conducted, it was found that a majority
              of people believe that farm-workers will become obsolete in the
              next 1-5 years by the hands of automation. This is a staggering
              statistic and truely shows the extent and severity of this
              problem. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Suspendisse tempus libero vel placerat condimentum. Vestibulum at
              sodales leo. Duis venenatis eleifend bibendum. Nulla facilisi.
              Donec a nulla arcu. Aenean fermentum sagittis ornare. Nulla
              facilisi. Duis lorem diam, porta mattis sagittis ut, rutrum sit
              amet risus. Morbi nec commodo leo. Nunc tincidunt fermentum justo,
              ac facilisis elit. Sed nec ligula facilisis purus mattis
              pellentesque eget ac leo. Donec ut lectus eget lorem sagittis
              feugiat. Suspendisse leo erat, euismod ac sagittis eget, rutrum ac
              lorem. Curabitur quis dolor fermentum, pharetra tellus sit amet,
              laoreet augue. Donec et diam condimentum, auctor dui sed, bibendum
              ipsum. Nunc luctus mollis ullamcorper. Duis ornare libero leo,
              vitae semper eros luctus eu. Fusce efficitur justo nunc, in
              tincidunt risus egestas id.
            </div>
            <div class="col-5">
              <!-- Github pages: src="/Agriculture/farmer-automation-survey.png" -->
              <!-- Not Github pages: src="/farmer-automation-survey.png" -->
              <img
                src="/farmer-automation-survey.png"
                alt="Survey results"
                class="img-thumbnail shadow"
              />
            </div>
          </div>
          <br /><br /><br />
          <div class="row">
            <div class="col-5">
              <!-- Github pages: src="/Agriculture/farming-robot.jpg" -->
              <!-- Not Github pages: src="/farming-robot.jpg" -->
              <img
                src="/farming-robot.jpg"
                alt="Robot automating farming work"
                class="img-thumbnail shadow"
              />
            </div>
            <div class="col-7">
              On the other hand, in some areas of america, this may be a
              beneficial thing. Approximately half of America's farmworkers are
              in the country illegally, and the possibility of automation would
              serve to legitimise the employing practices of some companies by
              cutting out the human middleman. Sed sollicitudin mi et tincidunt
              Maecenas tincidunt sodales arcu, vitae sodales eros scelerisque
              sed. Morbi vitae metus viverra, dignissim lacus eu, interdum nunc.
              Fusce imperdiet pellentesque sem, ac molestie urna sagittis sed.
              Cras suscipit nibh ac vulputate finibus. Praesent id tempor felis.
              Donec hendrerit erat libero, ac interdum urna cursus at. Nam ut
              commodo magna. Maecenas pharetra congue sem, ut fringilla turpis
              consequat ut. Vestibulum vel justo dolor. Etiam sollicitudin arcu
              a sagittis tincidunt. Praesent at tellus sed elit congue
              sollicitudin vitae eget leo. Aliquam erat volutpat.
            </div>
          </div>
          <small
            >*Views, opinions, etc. expressed do not reflect those of the
            author. This is just an example site</small
          >
        </div>
      </div>
    </div>
    <footer class="footer">
      <div class="footerWrapper">
        <span class="text-white-50"
          >&copy; Niseyami 2020 / Github:
          <a href="https://github.com/Niseyami" class="text-white-50"
            >https://github.com/Niseyami</a
          ></span
        >
      </div>
    </footer>
  </div>
</template>

<style scoped lang="scss">
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
  margin-bottom: 0.5rem;
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

a {
  color: #35495e;
}

a:hover {
  color: #2c3d4e;
}

.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 2.5rem;
  line-height: 2.5rem;
  background-color: #2e3338;
}

.footerWrapper {
  margin-left: 2rem;
}

@media (max-width: 416px) {
  .footer {
    height: 3.5rem;
    line-height: 1rem;
    background-color: #2e3338;
    div {
      margin-top: 0.75rem;
    }
  }
}

@media (max-width: 445px) {
  .footerWrapper {
    margin-left: 1rem;
  }
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

<script>
import Navbar from '~/components/Navbar.vue'

export default {
  components: {
    Navbar
  },
  head: {
    title: 'Agriculture'
  }
}
</script>
