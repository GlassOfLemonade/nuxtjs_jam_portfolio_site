<template>
  <section class="hero is-large">
    <div class="hero-body">
      <div class="container">
        <h1 class="title is-1">{{ content.title }}</h1>
        <h2 class="subtitle is-3">{{ content.description }}</h2>
        <!-- <a
          href="/kevin_tian_resume.pdf"
          target="_blank"
          rel="noopener noreferrer"
          class="button is-light is-primary"
        >
          Resume
        </a> -->
        <nuxt-content :document="content" />
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    content: {
      type: Object,
      default: () => {},
    },
  },
}
</script>
<style lang="scss">
section.hero {
  padding-top: $navbar-height; // match header height
}
</style>
