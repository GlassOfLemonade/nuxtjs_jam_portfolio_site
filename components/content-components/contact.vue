<template>
  <section id="section-contact" class="section">
    <div class="content"><h1 class="section-title">Contact Me</h1></div>
    <div class="container">
      <i class="fas fa-envelope-square"></i>
      <div class="content">
        <p>Find me and my work below!</p>
      </div>
      <div class="columns">
        <div class="column">
          <figure class="image">
            <a
              href="https://github.com/GlassOfLemonade"
              target="_blank"
              rel="noopener noreferrer"
            >
              <font-awesome-icon
                :icon="['fab', 'github']"
                style="font-size: 2em;"
              />
            </a>
          </figure>
        </div>
        <div class="column">
          <figure class="image">
            <a
              href="https://www.linkedin.com/in/kevin-tian-985bb29b"
              target="_blank"
              rel="noopener noreferrer"
            >
              <font-awesome-icon
                :icon="['fab', 'linkedin']"
                style="font-size: 2em;"
              />
            </a>
          </figure>
        </div>
        <div class="column">
          <figure class="image">
            <a href="mailto:ktian0257@gmail.com">
              <font-awesome-icon
                :icon="['fas', 'envelope-square']"
                style="font-size: 2em;"
              />
            </a>
          </figure>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.content p {
  text-align: center;
}

.columns {
  justify-content: center;
}

.column {
  flex: none;
  align-self: center;
}

figure.image,
figure.image img {
  max-width: 64px;
  max-height: 64px;
}
</style>
