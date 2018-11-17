<template>
  <div
    id="nav"
    class="nav-container"
  >
    <nav class="nav">
      <div class="nav-brand-container">
        <span class="nav-brand">Andrew Mason</span>
      </div>
      <div
        v-if="open === true"
        id="sidebar-close"
      >
        <button
          class="nav-toggle hover:text-blue-darkest hover:border-white hover:bg-white"
          @click="toggle">
          <svg
            class="nav-toggle-icon"
            role="button"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20">
            <path
              d="M10 8.586L2.929 1.515 1.515 2.929 8.586 10l-7.071 7.071 1.414 1.414L10 11.414l7.071 7.071 1.414-1.414L11.414 10l7.071-7.071-1.414-1.414L10 8.586z"
            />
          </svg>
        </button>
      </div>
      <div
        v-else
        id="sidebar-open"
      >
        <button
          class="nav-toggle hover:text-blue-darkest hover:border-white hover:bg-white"
          @click="toggle">
          <svg
            class="nav-toggle-icon"
            role="button"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20">
            <path
              d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"
            />
          </svg>
        </button>
      </div>
      <div
        :class="open ? 'block': 'hidden'"
        class="navbar">
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
.nav-container {
  @apply font-sans antialiased bg-blue-darkest w-full;
}
.nav {
  @apply flex items-center justify-between flex-wrap px-6 py-2;
}
.nav-brand-container {
  @apply flex items-center flex-no-shrink text-white ml-0;
}
.nav-brand {
  @apply font-semibold text-xl;
}
.nav-toggle {
  @apply items-center px-3 py-2 rounded text-white;
}
.nav-toggle-icon {
  @apply fill-current w-4 h-4 cursor-pointer align-text-bottom;
}
.nav-link {
  @apply no-underline block mt-4 text-white;
}
.nav-btn {
  @apply no-underline inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white mt-4;
}
.navbar {
  @apply w-full flex-grow text-right;
}
#sidebar-open {
  @apply block;
}
@screen sm {
  .nav-container {
    @apply min-h-screen fixed w-1/4;
  }
  .nav {
    @apply flex-col;
  }
  .nav-brand-container {
    @apply w-full mt-4;
  }
  .nav-link {
    @apply block mt-8;
  }
  .nav-btn {
    @apply mt-8;
  }
  .navbar {
    @apply flex flex-col w-full text-left;
  }
  #sidebar-open {
    @apply hidden;
  }
}
@screen lg {
}
</style>
