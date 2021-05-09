<template>
  <div class="container">
    <div>
      <Hero :content="contentHero" />
      <About :content="contentAbout" />
      <Work :content="contentWork" />
      <Projects :content="projectList" />
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
    const projectList = await $content('projects')
      .where({ priority: { $lt: 8 } })
      .fetch()
      .then((result) =>
        result.sort((a, b) => {
          return a.priority - b.priority
        })
      )
    const projectArchive = await $content('projects')
      .where({
        priority: { $gte: 8 },
      })
      .fetch()
    const contentWork = await $content('jobs').fetch()

    return {
      contentHero,
      contentAbout,
      projectList,
      projectArchive,
      contentWork,
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
