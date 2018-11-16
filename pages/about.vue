<template>
  <section class="container">
    <div>
      <h1 class="title">About</h1>
      <h2 class="subtitle">About subtitle</h2>
    </div>
  </section>
</template>


<style>
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  color: #35495e;
  letter-spacing: 1px;
  @apply text-lg mb-2;
}

@screen md {
  .title {
    @apply text-4xl;
  }
}

.subtitle {
  font-weight: 300;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  @apply text-base;
}

@screen md {
  @apply text-2xl;
}

.links {
  padding-top: 15px;
}
</style>
