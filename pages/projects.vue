<template>
  <section class="container">
    <h1 class="title">Projects</h1>
    <div id="projects" class="projects-container">
      <h1 class="subtitle">Projects I Contribute To</h1>
      <div class="project-grid">
        <div v-for="item in contributed" :key="item.name">
          <div class="project-container">
            <div
              class="bg-white mx-auto max-w-sm shadow-lg rounded-lg overflow-hidden"
            >
              <div class="px-6 py-4">
                <div
                  class="inline-flex rounded-full bg-blue-primary p-4 mb-4"
                  v-html="item.icon"
                />
                <div class="text-center">
                  <div class="mb-4">
                    <p class="text-xl leading-tight">{{ item.name }}</p>
                  </div>
                  <div>
                    <a
                      :href="item.link"
                      target="_blank"
                      class="button--blue-outline mb-8"
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
      <h1 class="subtitle">My Projects</h1>
      <div class="project-grid">
        <div v-for="item in myProjects" :key="item.name">
          <div class="project-container">
            <div
              class="bg-white mx-auto max-w-sm shadow-lg rounded-lg overflow-hidden"
            >
              <div class="px-6 py-4">
                <div
                  class="inline-flex rounded-full bg-blue-primary p-4 mb-4"
                  v-html="item.icon"
                />
                <div class="text-center">
                  <div class="mb-4">
                    <p class="text-xl leading-tight">{{ item.name }}</p>
                  </div>
                  <div>
                    <a
                      :href="item.link"
                      target="_blank"
                      class="button--blue-outline mb-8"
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
      <h1 class="subtitle">Demos</h1>
      <div class="project-grid">
        <div v-for="item in demos" :key="item.name">
          <div class="project-container">
            <div
              class="bg-white mx-auto max-w-sm shadow-lg rounded-lg overflow-hidden"
            >
              <div class="px-6 py-4">
                <div
                  class="inline-flex rounded-full bg-blue-primary p-4 mb-4"
                  v-html="item.icon"
                />
                <div class="text-center">
                  <div class="mb-4">
                    <p class="text-xl leading-tight">{{ item.name }}</p>
                  </div>
                  <div>
                    <a
                      :href="item.link"
                      target="_blank"
                      class="button--blue-outline mb-8"
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
          name: 'Awesome Lucky',
          icon: simpleIcons['Ruby'].svg,
          link: 'https://github.com/andrewmcodes/awesome-lucky'
        },
        {
          name: 'Ruby & Rails Resources',
          icon: simpleIcons['Ruby'].svg,
          link: 'https://github.com/andrewmcodes/ruby-rails-resources'
        }
      ],
      demos: [
        {
          name: 'Awesome Lucky',
          icon: simpleIcons['Ruby'].svg,
          link: 'https://github.com/andrewmcodes/awesome-lucky'
        },
        {
          name: 'Ruby & Rails Resources',
          icon: simpleIcons['Ruby'].svg,
          link: 'https://github.com/andrewmcodes/ruby-rails-resources'
        }
      ],
      contributed: [
        {
          name: 'release-notes',
          icon: simpleIcons['Ruby'].svg,
          link: 'https://github.com/dvmonroe/release-notes'
        },
        {
          name: 'homebrew-cask',
          icon: simpleIcons['PowerShell'].svg,
          link: 'https://github.com/Homebrew/homebrew-cask/pull/52809'
        },
        {
          name: 'Archipelago',
          icon: simpleIcons['React'].svg,
          link: 'https://github.com/npezza93/archipelago'
        }
      ]
    }
  }
}
</script>

<style>
.blue-primary {
  color: hsl(229.09, 90%, 62%);
}
.bg-blue-primary {
  background-color: hsl(229.09, 90%, 62%);
}
.border-blue-primary {
  border-color: hsl(229.09, 90%, 62%);
}
.subtitle {
  @apply text-4xl font-light;
}
.category-title {
  @apply text-left text-2xl mt-6 mb-4 font-light;
}
.projects-container {
  @apply px-4 mt-8;
}
.project-container {
  @apply mb-4;
}
.project-grid {
  @apply flex flex-wrap justify-between overflow-hidden;
}
.project-grid svg {
  @apply w-8 h-8 mx-auto relative z-10;
  fill: white;
}
@screen sm {
  .projects-container {
    @apply px-8;
  }
}
</style>
