<template>
  <div class="container">
    <div>
      <Hero :content="hero" />
      <About />
      <Work />
      <Projects />
      <Contact />
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const hero = await $content('hero').fetch()

    return {
      hero,
    }
  },
}
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.links {
  padding-top: 15px;
}
</style>
