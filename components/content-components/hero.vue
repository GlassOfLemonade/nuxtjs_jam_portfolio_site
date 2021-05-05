<template>
  <section class="hero is-large">
    <div class="hero-body">
      <div class="container">
        <h1 class="title is-1">Kevin Tian</h1>
        <h2 class="subtitle is-3">Front End Software Engineer</h2>
        <a
          href="https://docs.google.com/document/d/1H0K7FYrkoIBSl-DTll1vHAMHKzqkhjjQJOk6zlL8VUQ/edit?usp=sharing"
          target="_blank"
          rel="noopener noreferrer"
          class="button is-light is-primary"
        >
          Resume
        </a>
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
