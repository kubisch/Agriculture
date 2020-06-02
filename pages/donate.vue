<template>
  <div style="position: relative; min-height: 100vh;">
    <navbar />
    <div
      class="container main-content"
      style="margin-top: 4rem; padding-bottom: 4rem;"
    >
      <div class="card shadow-sm mb-3">
        <div class="row no-gutters">
          <div class="col-md-4">
            <!-- Github pages: src="/Agriculture/donate-image.jpg" -->
            <!-- Not Github pages: src="/donate-image.jpg" -->
            <img
              src="/Agriculture/donate-image.jpg"
              class="card-img"
              alt="Donation image"
            />
          </div>
          <div class="col-md-8">
            <div class="card-body">
              <h5 class="card-title title">Donate</h5>
              <p class="card-text">
                Help us spread the word, with a small donation. (Not a real,
                donation box don't try it). Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Placeat illo, sit officiis
                repellendus harum quae expedita, deleniti nisi tempora
                doloremque et corporis id vel explicabo fuga fugiat error
                distinctio delectus.
              </p>
              <hr />
              <div class="input-group mb-3">
                <div class="input-group-prepend">
                  <div class="btn-group btn-group-toggle" data-toggle="buttons">
                    <label class="btn btn-secondary active">
                      <input
                        id="input1"
                        type="radio"
                        name="options"
                        autocomplete="off"
                      />
                      $1
                    </label>
                    <label class="btn btn-secondary">
                      <input
                        id="input2"
                        type="radio"
                        name="options"
                        autocomplete="off"
                      />
                      $5
                    </label>
                    <label class="btn btn-secondary">
                      <input
                        id="input3"
                        type="radio"
                        name="options"
                        autocomplete="off"
                      />
                      $10
                    </label>
                    <label class="btn btn-secondary">
                      <input
                        id="input4"
                        type="radio"
                        name="options"
                        autocomplete="off"
                      />
                      $25
                    </label>
                    <label class="btn btn-secondary">
                      <input
                        id="input5"
                        type="radio"
                        name="options"
                        autocomplete="off"
                      />
                      $50
                    </label>
                    <label class="btn btn-secondary">
                      <input
                        id="otherButton"
                        type="radio"
                        name="options"
                        autocomplete="off"
                      />
                      Other
                    </label>
                  </div>
                </div>
                <div class="input-group-prepend">
                  <span id="dollarSign" class="input-group-text" hidden>$</span>
                </div>
                <input
                  id="otherBox"
                  type="text"
                  class="form-control"
                  placeholder="Amount"
                  disabled
                />
                <div class="input-group-prepend">
                  <button type="button" class="btn btn-primary">Donate</button>
                </div>
              </div>
            </div>
          </div>
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
    <script>
      $(function() {
        $('#otherButton').on('change', function() {
          if (this.checked) {
            document.getElementById('otherBox').disabled = false
            document.getElementById('dollarSign').hidden = false
          } else {
            document.getElementById('otherBox').disabled = true
          }
        })
      })
      $(function() {
        $('#input1').on('change', function() {
          if (this.checked) {
            document.getElementById('otherBox').disabled = true
            document.getElementById('dollarSign').hidden = true
          }
        })
      })
      $(function() {
        $('#input2').on('change', function() {
          if (this.checked) {
            document.getElementById('otherBox').disabled = true
            document.getElementById('dollarSign').hidden = true
          }
        })
      })
      $(function() {
        $('#input3').on('change', function() {
          if (this.checked) {
            document.getElementById('otherBox').disabled = true
            document.getElementById('dollarSign').hidden = true
          }
        })
      })
      $(function() {
        $('#input4').on('change', function() {
          if (this.checked) {
            document.getElementById('otherBox').disabled = true
            document.getElementById('dollarSign').hidden = true
          }
        })
      })
      $(function() {
        $('#input5').on('change', function() {
          if (this.checked) {
            document.getElementById('otherBox').disabled = true
            document.getElementById('dollarSign').hidden = true
          }
        })
      })
    </script>
  </div>
</template>

<style scoped lang="scss">
.input-group-append .btn,
.input-group-prepend .btn {
  z-index: 1;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
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
