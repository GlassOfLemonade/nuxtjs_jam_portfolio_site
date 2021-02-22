<template>
  <div class="container">
    <div>
      <Hero />
      <About />
      <Work />
      <Projects />
      <Contact />
    </div>
  </div>
</template>

<script>
export default {}
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
