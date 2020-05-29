<template>
  <div style="position: relative; min-height: 100vh;">
    <navbar />
    <div class="container main-content">
      <div class="row justify-content-between" style="margin-top: 4rem">
        <div class="col-sm-7" style="margin-bottom: 6rem;">
          <div class="card shadow-sm">
            <div class="card-body">
              <h5 class="card-title title">Contact us</h5>
              <p class="card-text">
                We'd love to hear from you!
              </p>
              <hr />
              <p class="card-text">
                Feedback:
                <a href="mailto:feedback@example.org">feedback@example.org</a
                ><br />
                Phone: <a href="tel:+12065550100">+1 206 555 0100</a><br />
                Fax: <a href="tel:+61212345678">+61 2 1234 5678</a><br />
                Legal Inquiries:
                <a href="mailto:legal@example.org">legal@example.org</a>
              </p>
              <hr />
              <h5 class="card-title title" style="font-size:2rem">
                Got a question?
              </h5>
              <form>
                <div class="form-group">
                  <label for="inputEmail4">Email</label>
                  <input
                    id="inputEmail"
                    type="email"
                    class="form-control"
                    placeholder="Email"
                    aria-describedby="emailHelp"
                  />
                  <small id="emailHelp" class="form-text text-muted"
                    >We'll never share your email with anyone else.</small
                  >
                </div>
                <div class="form-group">
                  <label for="TextArea">What do you want to know?</label>
                  <textarea
                    id="TextArea"
                    class="form-control"
                    rows="3"
                  ></textarea>
                </div>
                <button type="submit" class="btn btn-primary">Send</button>
              </form>
            </div>
          </div>
        </div>
        <div class="col-sm-5">
          <div class="card shadow-sm" style="margin-bottom: 6rem;">
            <div class="card-body">
              <h5 class="card-title title" style="font-size: 2rem;">
                Find us on social media
              </h5>
              <hr />
              <p class="card-text">
                With supporting text below as a natural lead-in to additional
                content.
              </p>
              <div>
                <a href=""><i class="fab fa-steam-square fa-5x"></i></a>
                <a href=""><i class="fab fa-facebook-square fa-5x"></i></a>
                <a href=""><i class="fab fa-github-square fa-5x"></i></a>
                <a href=""><i class="fab fa-snapchat-square fa-5x"></i></a>
                <a href=""><i class="fab fa-twitter-square fa-5x"></i></a>
                <a href=""><i class="fab fa-tumblr-square fa-5x"></i></a>
                <a href=""><i class="fab fa-instagram-square fa-5x"></i></a>
                <a href=""><i class="fab fa-linkedin fa-5x"></i></a>
                <a href=""><i class="fab fa-youtube-square fa-5x"></i></a>
                <a href=""><i class="fab fa-reddit-square fa-5x"></i></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footer class="footer">
      <div style="margin-left: 2rem;">
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

@media (max-width: 445px) {
  .footer {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 5rem;
    line-height: 2.5rem;
    background-color: #2e3338;
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
