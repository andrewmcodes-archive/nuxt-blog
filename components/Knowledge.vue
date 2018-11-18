<template>
  <div
    id="knowledge"
    class="knowledge-container"
  >
    <h1 class="subtitle">Language &amp; Tool Experience</h1>
    <div class="line-seperator" />
    <h2
      class="category-title"
    >
      Experimented with...
    </h2>
    <div
      class="icon-grid"
    >
      <div
        v-for="item in experimented"
        :key="item.name"
        class="icon-container"
      >
        <div class="tile">
          <svg
            v-html="item.icon"
          />
          <div class="tile-seperator" />
          <h3>{{ item.name }}</h3>
        </div>
      </div>
    </div>
    <h2
      class="category-title"
    >
      Familiar with...
    </h2>
    <div
      class="icon-grid"
    >
      <div
        v-for="item in famaliar"
        :key="item.name"
        class="icon-container"
      >
        <div class="tile">
          <svg
            v-html="item.icon"
          />
          <div class="tile-seperator" />
          <h3>{{ item.name }}</h3>
        </div>
      </div>
    </div>
    <h2
      class="category-title"
    >
      Proficient with...
    </h2>
    <div
      class="icon-grid"
    >
      <div
        v-for="item in proficient"
        :key="item.name"
        class="icon-container"
      >
        <div class="tile">
          <svg
            v-html="item.icon"
          />
          <div class="tile-seperator" />
          <h3>{{ item.name }}</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const simpleIcons = require('simple-icons')

export default {
  data() {
    return {
      experimented: [
        { name: 'GraphQL', icon: simpleIcons['GraphQL'].svg },
        { name: 'Gulp', icon: simpleIcons['Gulp'].svg },
        { name: 'D3.js', icon: simpleIcons['D3.js'].svg },
        { name: 'Firebase', icon: simpleIcons['Firebase'].svg },
        { name: 'Kibana', icon: simpleIcons['Kibana'].svg },
        { name: 'Salesforce', icon: simpleIcons['Salesforce'].svg },
        { name: 'Stripe', icon: simpleIcons['Stripe'].svg },
        { name: 'Redux', icon: simpleIcons['Redux'].svg }
      ],
      famaliar: [
        { name: 'Gatsby', icon: simpleIcons['Gatsby'].svg },
        { name: 'Jekyll', icon: simpleIcons['Jekyll'].svg },
        { name: 'Redis', icon: simpleIcons['Redis'].svg },
        { name: 'Sentry', icon: simpleIcons['Sentry'].svg },
        { name: 'Cloudflare', icon: simpleIcons['Cloudflare'].svg },
        { name: 'Node.js', icon: simpleIcons['Node.js'].svg },
        { name: 'MongoDB', icon: simpleIcons['MongoDB'].svg },
        { name: 'Travis CI', icon: simpleIcons['Travis CI'].svg },
        { name: 'Vue.js', icon: simpleIcons['Vue.js'].svg },
        { name: 'React', icon: simpleIcons['React'].svg },
        { name: 'Java', icon: simpleIcons['Java'].svg },
        { name: 'Docker', icon: simpleIcons['Docker'].svg },
        { name: 'jQuery', icon: simpleIcons['jQuery'].svg },
        { name: 'PHP', icon: simpleIcons['PHP'].svg },
        { name: 'ESLint', icon: simpleIcons['ESLint'].svg },
        { name: 'Heroku', icon: simpleIcons['Heroku'].svg },
        { name: 'CirclecCI', icon: simpleIcons['CircleCI'].svg }
      ],
      proficient: [
        { name: 'Sass', icon: simpleIcons['Sass'].svg },
        { name: 'NPM', icon: simpleIcons['NPM'].svg },
        { name: 'Rails', icon: simpleIcons['Rails'].svg },
        { name: 'Ruby', icon: simpleIcons['Ruby'].svg },
        { name: 'HTML5', icon: simpleIcons['HTML5'].svg },
        { name: 'CSS3', icon: simpleIcons['CSS3'].svg },
        { name: 'Git', icon: simpleIcons['Git'].svg },
        { name: 'JavaScript', icon: simpleIcons['JavaScript'].svg },
        { name: 'Netlify', icon: simpleIcons['Netlify'].svg },
        { name: 'Python', icon: simpleIcons['Python'].svg },
        { name: 'MySQL', icon: simpleIcons['MySQL'].svg },
        { name: 'Bootstrap', icon: simpleIcons['Bootstrap'].svg }
      ]
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
.subtitle {
  @apply text-4xl font-light;
}
.category-title {
  @apply text-left text-2xl mt-6 mb-4 font-light;
}
.knowledge-container {
  @apply px-4 mt-8;
}
.icon-grid {
  @apply flex flex-wrap overflow-hidden;
}
.icon-grid svg {
  @apply w-16 h-16 mx-auto;
  fill: #12283a;
}
.icon-grid svg::after {
  content: '';
}
.tile-seperator {
  @apply bg-blue opacity-50 mt-4;
  height: 1px;
  width: 64px;
}
.icon-container {
  @apply flex flex-col mx-auto mb-4 w-auto;
}
.icon-container h3 {
  @apply mt-3 font-normal;
}
.tile {
  @apply rounded-lg p-4 bg-white shadow;
}
@screen sm {
  .knowledge-container {
    @apply px-8;
  }
  .icon-grid svg {
    @apply w-8 h-8;
  }
  .icon-container {
    @apply w-1/4;
  }
  .tile {
    @apply rounded-lg mx-2 py-4 px-2 bg-white shadow-md;
  }
  .tile-seperator {
    @apply mt-0;
  }
}
@screen md {
  .icon-grid svg {
    @apply w-16 h-16;
  }
  .tile {
    @apply mx-4 px-4;
  }
}
</style>
