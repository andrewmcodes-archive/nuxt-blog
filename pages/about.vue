<template>
  <section class="container">
    <h1 class="title">About</h1>
    <Bio />
    <Knowledge />
  </section>
</template>

<script>
import Knowledge from '~/components/Knowledge.vue'
import Bio from '~/components/Bio.vue'

export default {
  components: {
    Knowledge,
    Bio
  }
}
</script>

<style>
.container {
  @apply text-left mt-4;
}
@screen md {
  .container {
    @apply mt-8;
  }
}
.line-seperator {
  @apply bg-blue opacity-50 -mt-2 mb-4;
  height: 1px;
  width: 64px;
}
</style>
