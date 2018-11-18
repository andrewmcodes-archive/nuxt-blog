<template>
  <div class="lightbulb">
    <img src="~/assets/images/lightbulb.svg" alt="Logo" width="240px" />
  </div>
</template>

<style>
.lightbulb img {
  @apply mb-4;
}
@screen md {
  .lightbulb img {
    @apply mb-8;
  }
}
</style>
