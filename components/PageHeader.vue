<template>
  <div class="page-header">
    <div class="inner relative">
      <div
        class="overlay absolute h-full w-full top-0 left-0 right-0 bottom-0 animated fadeIn slower"
      ></div>
      <div
        class="hero bg-cover bg-center flex flex-col items-center justify-center text-white space-y-6 py-28 md:py-36 lg:py-44 px-4"
        :style="`background-image:url('/images/bg${bg}.jpg')`"
      >
        <h1 class="text-3xl lg:text-5xl capitalize animated fadeInUp slow">
          {{ title }}
        </h1>
        <article
          class="max-w-3xl text-md lg:text-xl text-center font-thin space-y-3 animated fadeIn delay-1s"
        >
          <slot></slot>
        </article>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageHeader',
  props: {
    title: {
      type: String,
      default: 'DLZ Media',
    },
    bg: {
      type: String,
      default: '1',
    },
  },
}
</script>

<style lang="scss" scoped>
.page-header {
  .hero {
    h1 {
      font-family: 'Zen Dots', cursive;
    }
  }
  .overlay {
    background: #00000060;
    filter: blur(8px);
  }
}
</style>
