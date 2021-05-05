<template>
  <section id="section-about" class="section">
    <div class="content"><h1 class="section-title">About Me</h1></div>
    <div class="container">
      <div class="columns">
        <div class="column">
          <div class="content">
            <p>
              I'm Kevin Tian, a front-end engineer based in Los Angeles, CA.
            </p>
            <p>
              I'm a mostly self taught software developer, and like to challenge
              myself to new experiences by participating in hackathons and game
              jams.
            </p>
            <p>
              On a professional level I create connected applications and
              experiences on the web. With my most recent position at
              CauseForce, I was given an introduction into the world of web
              engineering and took opportunities where I could to tackle new
              problems, work with new technologies, and create connected and
              personalized web applications.
            </p>
            <p>Web technologies I've used:</p>
            <nuxt-content :document="content" />
          </div>
        </div>
        <!-- <div class="column">
          <figure class="image">
            <img
              class="is-rounded"
              src="https://bulma.io/images/placeholders/256x256.png"
              alt="my picture"
            />
          </figure>
        </div> -->
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
<style lang="scss"></style>
