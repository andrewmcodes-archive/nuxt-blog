<template>
  <section class="container">
    <h1 class="title">Projects</h1>
    <div id="projects" class="projects-container">
      <h1 class="subtitle">My Projects</h1>
      <div class="project-grid">
        <div v-for="item in myProjects" :key="item.name">
          <div class="project-container">
            <div
              class="bg-white mx-auto max-w-sm shadow-lg rounded-lg overflow-hidden"
            >
              <div class="px-6 py-4">
                <svg
                  class="block w-12 h-12 rounded-full mx-auto mb-4"
                  v-html="item.icon"
                />
                <div class="text-center">
                  <div class="mb-4">
                    <p class="text-xl leading-tight">Adam Wathan</p>
                  </div>
                  <div>
                    <a
                      href="https://github.com/andrewmcodes"
                      target="_blank"
                      class="button--grey mb-8"
                    >
                      GitHub
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
const simpleIcons = require('simple-icons')

export default {
  data() {
    return {
      myProjects: [
        {
          name: 'vscode-ruby',
          icon: simpleIcons['GitHub'].svg,
          link: 'https://github.com/rubyide/vscode-ruby'
        },
        { name: 'Twitter', icon: simpleIcons['Twitter'].svg, link: 'x' },
        { name: 'LinkedIn', icon: simpleIcons['LinkedIn'].svg, link: 'x' },
        { name: 'CodePen', icon: simpleIcons['CodePen'].svg, link: 'x' }
      ]
    }
  }
}
</script>

<style>
.subtitle {
  @apply text-4xl font-light;
}
.category-title {
  @apply text-left text-2xl mt-6 mb-4 font-light;
}
.projects-container {
  @apply px-4 mt-8;
}
.project-grid {
  @apply flex flex-wrap overflow-hidden;
}
.icon-grid svg {
  @apply w-12 h-12 mx-auto;
  fill: hsl(229.09, 90%, 52%);
}
.blue-primary {
  color: hsl(229.09, 90%, 62%);
}
.bg-blue-primary {
  background-color: hsl(229.09, 90%, 92%);
}
.border-blue-primary {
  border-color: hsl(229.09, 90%, 62%);
}
@screen sm {
  .projects-container {
    @apply px-8;
  }
}
</style>
