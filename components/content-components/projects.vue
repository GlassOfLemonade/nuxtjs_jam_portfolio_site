<template>
  <section id="section-projects" class="section">
    <div class="content"><h1 class="section-title">Projects</h1></div>
    <div class="container">
      <div class="tile is-ancestor">
        <reuse-card
          v-for="index in 4"
          :key="index"
          :content="content[index - 1]"
        />
      </div>

      <div class="tile is-ancestor">
        <reuse-card
          v-for="index in 4"
          :key="index"
          :content="content[index + 3]"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    content: {
      type: Array,
      default: () => {},
    },
  },
}
</script>

<style lang="scss" scoped>
article.box {
  div.container {
    display: flex;
    padding-bottom: 0.5rem;
  }
}
</style>
