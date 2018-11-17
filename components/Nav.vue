<template>
  <div
    id="nav"
    class="font-sans antialiased sm:h-screen bg-blue-darkest"
  >
    <nav class="flex sm:flex-col items-center justify-between flex-wrap p-6">
      <div class="flex sm:w-full items-center flex-no-shrink text-white ml-0">
        <span class="font-semibold text-xl">Andrew Mason</span>
      </div>
      <div class="block sm:hidden">
        <button
          class="flex items-center px-3 py-2 border rounded text-white border-white hover:text-blue-darkest hover:border-white hover:bg-white"
          @click="toggle">
          <svg
            class="fill-current h-3 w-3"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
        </button>
      </div>
      <div
        :class="open ? 'block': 'hidden'"
        class="w-full flex-grow sm:flex sm:flex-col sm:w-full text-right sm:text-left">
        <div class="text-sm">
          <a
            href="#responsive-header"
            class="nav-link">
            Docs
          </a>
          <a
            href="#responsive-header"
            class="nav-link">
            Examples
          </a>
          <a
            href="#responsive-header"
            class="nav-link">
            Blog
          </a>
        </div>
        <div>
          <a
            href="#"
            class="nav-btn">Contact</a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      open: false
    }
  },
  methods: {
    toggle() {
      this.open = !this.open
    }
  }
}
</script>

<style>
.nav-link {
  @apply no-underline block mt-4 text-white;
}
.nav-btn {
  @apply no-underline inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white mt-4;
}
/* @variants hover {
  .nav-btn {
    @apply border-transparent text-teal bg-white;
  }
} */
@screen sm {
  .nav-link {
    @apply block mt-8;
  }
  .nav-btn {
    @apply mt-8;
  }
}
@screen md {
  .nav-link {
    /* @apply mr-4; */
  }
}
</style>
