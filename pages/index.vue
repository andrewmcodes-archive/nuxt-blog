<template>
  <section class="container">
    <div class="min-h-screen">
      <logo/>
      <h1 class="title">
        Andrew Mason
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
