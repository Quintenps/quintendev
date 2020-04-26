<template>
  <div>
    <div class="container">
      <nav class="navbar section">
        <div class="navbar-brand">
          <p class="logo navbar-item">
            QUINTENPEELS
          </p>
          <div
            class="navbar-burger"
            :class="{ 'is-active': showNav }"
            @click="showNav = !showNav"
          >
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>
        <div class="navbar-menu" :class="{ 'is-active': showNav }">
          <div class="navbar-end is-lowercase">
            <nuxt-link
              to="/"
              class="navbar-item"
              @click.native="showNav = !showNav"
            >
              About
            </nuxt-link>
            <nuxt-link
              to="work"
              class="navbar-item"
              @click.native="showNav = !showNav"
            >
              Work
            </nuxt-link>
            <nuxt-link
              to="contact"
              class="navbar-item"
              @click.native="showNav = !showNav"
            >
              Contact
            </nuxt-link>
          </div>
        </div>
      </nav>
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showNav: false
    }
  }
}
</script>
