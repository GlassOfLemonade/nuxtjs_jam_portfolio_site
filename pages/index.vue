<template>
  <div class="container">
    <div>
      <hero />
      <about />
    </div>
  </div>
</template>

<script>
import hero from '~/components/content-components/hero'
import about from '~/components/content-components/about'

export default {
  components: {
    hero,
    about,
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
