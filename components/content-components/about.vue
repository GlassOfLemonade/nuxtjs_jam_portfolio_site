<template>
  <section id="section-about" class="section">
    <div class="content"><h1 class="section-title">About Me</h1></div>
    <div class="container">
      <div class="columns">
        <div class="column is-two-thirds">
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
              CauseForce, which also happens to be my first professional
              experience in software, I was given an introduction into the world
              of web engineering and took opportunities where I could to tackle
              new problems, work with new technologies, and create connected and
              personalized web applications.
            </p>
            <p>Web technologies I've used:</p>
            <ul>
              <li>
                Core web programming languages: HTML, (S)CSS, Javascript
                ES6+/TypeScript
              </li>
              <li>Javascript frameworks: Vue.js, Angular, React</li>
              <li>Server-side: Node.js, Express, C#</li>
              <li>CSS frameworks: Tailwind, Bulma</li>
              <li>Platforms: Heroku, Netlify</li>
              <li>WordPress</li>
            </ul>
          </div>
        </div>
        <div class="column">
          <figure class="image">
            <picture>
              <source
                size="(max-width: 768px) 256px, 
                    350px"
                srcset="
                  /kevin_tian_picture-512w.webp   512w,
                  /kevin_tian_picture-1024w.webp 1024w
                "
                type="image/webp"
              />
              <img
                class="is-rounded"
                size="(max-width: 768px) 256px, 
                    350px"
                srcset="
                  /kevin_tian_picture-512w.jpg   512w,
                  /kevin_tian_picture-1024w.jpg 1024w
                "
                src="/kevin_tian_picture-512w.jpg"
                alt="my picture"
              />
            </picture>
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
figure.image {
  max-width: 350px;
  margin: 0 auto;
}
</style>
