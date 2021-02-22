<template>
  <footer class="footer">
    <div class="content has-text-centered">
      <p>
        Powered by
      </p>
    </div>
    <div class="container">
      <div class="columns credits">
        <div class="column">
          <figure class="image">
            <a
              href="https://nuxtjs.org/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img src="~assets/nuxt-white.svg" alt="Nuxt js logo" />
            </a>
          </figure>
        </div>
        <div class="column">
          <figure class="image">
            <a
              href="https://vuejs.org/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="~assets/277px-Vue.js_Logo_2.svg.png"
                alt="Vue js logo"
              />
            </a>
          </figure>
        </div>
        <div class="column">
          <figure class="image">
            <a
              href="https://bulma.io"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="https://bulma.io/images/made-with-bulma.png"
                alt="Made with Bulma"
                width="128"
                height="24"
              />
            </a>
          </figure>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.credits {
  justify-content: center;
}
.column {
  flex: none;
  align-self: center;
}

figure.image,
figure.image img {
  max-width: 128px;
  max-height: 128px;
}
</style>
