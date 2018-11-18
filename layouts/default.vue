<template>
  <div class="sm:flex">
    <div
      id="nuxt-nav"
      class="absolute sm:relative z-10 w-full sm:w-1/4 lg:w-1/5 shadow sm:shadow-md"
    >
      <Nav />
    </div>
    <div class="sm:pt-0 relative sm:w-3/4 lg:w-4/5 bg-grey-lighter">
      <nuxt/>
    </div>
  </div>
</template>

<script>
import Nav from '~/components/Nav.vue'

export default {
  components: {
    Nav
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.blue-primary {
  color: hsl(229.09, 90%, 62%);
}
.bg-blue-primary {
  background-color: hsl(229.09, 90%, 62%);
}
.border-blue-primary {
  border-color: hsl(229.09, 90%, 62%);
}

.button--blue {
  display: inline-block;
  border-radius: 999px;
  text-decoration: none;
  padding: 10px 30px;
  @apply border text-white border-blue-primary bg-blue-primary;
}

.button--blue:hover {
  @apply shadow-lg;
}

.button--grey {
  display: inline-block;
  border-radius: 999px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.container {
  @apply min-h-screen flex flex-col justify-center items-center text-center mx-auto;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  color: #35495e;
  letter-spacing: 1px;
  @apply text-5xl mb-2;
}

.subtitle {
  font-weight: 300;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  @apply text-2xl;
}

.links {
  @apply pt-4;
}
#nuxt-nav {
  max-width: 192px;
}
</style>
