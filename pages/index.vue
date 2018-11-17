<template>
  <section class="container">
    <h1 class="title">
      Hello,<br> my name is Andrew
    </h1>
    <h2 class="subtitle">
      Welcome to my personal-site
    </h2>
    <div class="links">
      <a
        href="https://github.com/andrewmcodes"
        target="_blank"
        class="button--grey mb-8">GitHub</a>
      <router-link
        to="/about"
        class="button--blue">About
      </router-link>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
</style>
