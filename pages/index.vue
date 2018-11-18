<template>
  <section class="container">
    <Lightbulb />
    <h1 class="title">
      <span class="blue-primary">Hello,</span>my name is Andrew
    </h1>
    <h2 class="subtitle">Welcome to my personal-site</h2>
    <div class="links">
      <a
        href="https://github.com/andrewmcodes"
        target="_blank"
        class="button--blue-outline mb-8"
      >
        GitHub
      </a>
      <router-link to="/about" class="button--blue">About </router-link>
    </div>
  </section>
</template>
<script>
import Logo from '~/components/Logo.vue'
import Lightbulb from '~/components/Lightbulb.vue'
export default {
  components: {
    Logo,
    Lightbulb
  }
}
</script>
