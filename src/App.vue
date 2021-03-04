<template>
  <div id="app" class="">
    <div class="container">
      <nav class="navbar section">
        <div class="navbar-brand">
          <p class="logo navbar-item">bluedog</p>
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
            <router-link
              to="/"
              class="navbar-item"
              @click.native="showNav = !showNav"
            >
              About
            </router-link>
            <router-link
              to="work"
              class="navbar-item"
              @click.native="showNav = !showNav"
            >
              Work
            </router-link>
            <router-link
              to="contact"
              class="navbar-item"
              @click.native="showNav = !showNav"
            >
              Contact
            </router-link>
          </div>
        </div>
      </nav>
      <div class="section">
        <router-view />
      </div>
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
