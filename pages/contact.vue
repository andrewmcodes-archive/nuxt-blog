<template>
  <div
    id="contact"
    class="contact-container"
  >
    <h1 class="title">Contact</h1>
    <div
      v-for="item in icons"
      :key="item.name"
      class="icon-container"
    >
      <svg
        v-html="item.icon"
      />
    </div>
  </div>
</template>

<script>
const simpleIcons = require('simple-icons')

export default {
  data() {
    return {
      icons: [
        { name: 'GitHub', icon: simpleIcons['GitHub'].svg },
        { name: 'Twitter', icon: simpleIcons['Twitter'].svg },
        { name: 'LinkedIn', icon: simpleIcons['LinkedIn'].svg },
        { name: 'CodePen', icon: simpleIcons['CodePen'].svg }
      ]
    }
  }
}
</script>
<style>
.contact-container {
  @apply px-4 pt-8 w-full text-center h-screen bg-grey-lighter;
}
#contact .icon-container {
  @apply flex flex-col mx-auto mb-4 w-auto;
}
#contact .icon-container svg {
  @apply w-12 h-12 mx-auto mb-8;
  fill: #12283a;
}
#contact .title {
  @apply mb-8;
}
.line-seperator {
  @apply bg-blue opacity-50 mx-auto -mt-2 mb-4 text-center;
  height: 1px;
  width: 64px;
}
</style>
