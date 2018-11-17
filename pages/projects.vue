<template>
  <section class="container">
    <div>
      <h1 class="title">Projects</h1>
      <h2 class="subtitle">Projects subtitle</h2>
    </div>
    <div class="flex flex-col sm:flex-row">
      <div class="card">
        <img
          class="card-img"
          src="https://tailwindcss.com/img/card-top.jpg"
          alt="Sunset in the mountains">
        <div class="card-body">
          <div class="card-title">The Coldest Sunset</div>
          <p class="card-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
          </p>
        </div>
        <div class="card-footer">
          <span class="card-footer-link mr-2">#photography</span>
          <span class="card-footer-link mr-2">#travel</span>
          <span class="card-footer-link">#winter</span>
        </div>
      </div>
      <div class="card">
        <img
          class="card-img"
          src="https://tailwindcss.com/img/card-top.jpg"
          alt="Sunset in the mountains">
        <div class="card-body">
          <div class="card-title">The Coldest Sunset</div>
          <p class="card-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
          </p>
        </div>
        <div class="card-footer">
          <span class="card-footer-link mr-2">#photography</span>
          <span class="card-footer-link mr-2">#travel</span>
          <span class="card-footer-link">#winter</span>
        </div>
      </div>
    </div>

    <div class="flex flex-col sm:flex-row">
      <div class="card">
        <img
          class="card-img"
          src="https://tailwindcss.com/img/card-top.jpg"
          alt="Sunset in the mountains">
        <div class="card-body">
          <div class="card-title">The Coldest Sunset</div>
          <p class="card-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
          </p>
        </div>
        <div class="card-footer">
          <span class="card-footer-link mr-2">#photography</span>
          <span class="card-footer-link mr-2">#travel</span>
          <span class="card-footer-link">#winter</span>
        </div>
      </div>
      <div class="card">
        <img
          class="card-img"
          src="https://tailwindcss.com/img/card-top.jpg"
          alt="Sunset in the mountains">
        <div class="card-body">
          <div class="card-title">The Coldest Sunset</div>
          <p class="card-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
          </p>
        </div>
        <div class="card-footer">
          <span class="card-footer-link mr-2">#photography</span>
          <span class="card-footer-link mr-2">#travel</span>
          <span class="card-footer-link">#winter</span>
        </div>
      </div>
    </div>
  </section>
</template>


<style>
.card {
  @apply max-w-sm rounded overflow-hidden shadow-lg mx-4 mb-4;
}
.card-img {
  @apply w-full;
}
.card-body {
  @apply px-6 py-4;
}
.card-title {
  @apply font-bold text-xl mb-2;
}
.card-text {
  @apply text-grey-darker text-base;
}
.card-footer {
  @apply px-6 py-4;
}
.card-footer-link {
  @apply inline-block bg-grey-lighter rounded-full px-3 py-1 text-sm font-semibold text-grey-darker;
}
</style>
