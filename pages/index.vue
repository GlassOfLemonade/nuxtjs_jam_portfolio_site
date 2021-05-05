<template>
  <div class="container">
    <div>
      <Hero :content="contentHero" />
      <About :content="contentAbout" />
      <Work />
      <Projects />
      <Contact />
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const sectionContent = await $content('sections').fetch()
    const contentHero = sectionContent.find((el) => el.title === 'Hero')
    const contentAbout = sectionContent.find((el) => el.title === 'About')

    return {
      contentHero,
      contentAbout,
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
