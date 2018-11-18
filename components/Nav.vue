<template>
  <div
    id="nav"
    class="nav-container"
  >
    <nav class="nav">
      <div class="nav-brand-container">
        <a
          href="/"
          class="nav-brand">
          Andrew Mason
        </a>
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
        <div class="link-container">
          <a
            href="/about"
            class="nav-link">
            About
          </a>
          <ul class="list-reset">
            <li>
              <a
                href="/about#bio"
                class="nav-sublink">
                Bio
              </a>
            </li>
            <li>
              <a
                href="/about#knowledge"
                class="nav-sublink">
                Language &amp; Tool Experience
              </a>
            </li>
          </ul>
          <a
            href="/projects"
            class="nav-link">
            Projects
          </a>
          <a
            href="/oss"
            class="nav-link">
            OSS
          </a>
          <a
            href="/contact"
            class="nav-link">
            Contact
          </a>
        </div>
        <div class="icon-container">
          <div
            id="github"
            class="w-6 h-6"
            v-html="github"
          />
          <div
            id="twitter"
            class="w-6 h-6"
            v-html="twitter"
          />
          <div
            id="linkedin"
            class="w-6 h-6"
            v-html="linkedin"
          />
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
const simpleIcons = require('simple-icons')

export default {
  data() {
    return {
      open: false,
      github: simpleIcons['GitHub'].svg,
      twitter: simpleIcons['Twitter'].svg,
      linkedin: simpleIcons['LinkedIn'].svg
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
  @apply font-sans antialiased bg-white w-full;
}
.nav {
  @apply flex items-center justify-between flex-wrap py-2;
}
.nav-brand-container {
  @apply flex items-center flex-no-shrink text-blue-darkest ml-4;
}
.nav-brand {
  @apply font-light text-xl no-underline;
  color: #35495e;
}
.nav-toggle {
  @apply items-center px-3 py-2 rounded text-blue-darkest mr-2;
}
.nav-toggle-icon {
  @apply fill-current w-4 h-4 cursor-pointer align-text-bottom;
}
.nav-link {
  @apply no-underline block text-blue-darkest font-semibold text-base text-center shadow-inner py-4 align-text-bottom uppercase tracking-wide;
}
.nav-sublink {
  @apply hidden;
}
.nav-btn {
  @apply no-underline inline-block text-sm px-4 py-2 leading-none border rounded text-blue-darkest border-blue-darkest mt-4;
}
.navbar {
  @apply w-full flex-grow text-right;
}
.link-container {
  @apply pt-2 w-full;
}
#nav .icon-container {
  @apply hidden;
}
#sidebar-open {
  @apply block;
}
.navbar svg {
  @apply w-8 h-8 !important;
  fill: #12283a;
}
@screen sm {
  .nav-container {
    @apply fixed w-1/4;
  }
  .nav {
    @apply flex-col px-6 min-h-screen;
  }
  .nav-brand-container {
    @apply w-full mt-4 ml-0;
  }
  .nav-link {
    @apply block mt-8 text-left shadow-none;
  }
  .nav-sublink {
    @apply no-underline block text-grey-dark font-semibold text-xs text-left py-1 align-text-bottom;
  }
  .nav-sublink:hover {
    @apply text-blue;
  }
  .nav-btn {
    @apply mt-8;
  }
  .navbar {
    @apply flex flex-col justify-between w-full text-left;
  }
  #nav .icon-container {
    @apply flex flex-row justify-between mx-2 mb-4 !important;
  }
  #sidebar-open {
    @apply hidden;
  }
}
@screen md {
  .nav-container {
    @apply w-1/5;
  }
}
</style>
