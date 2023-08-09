<template>
  <section id="section-about" class="section">
    <div class="content"><h1 class="section-title">About Me</h1></div>
    <div class="container">
      <div class="columns">
        <div class="column is-two-thirds">
          <div class="content">
            <p>I'm Kevin Tian, a software engineer based in Los Angeles, CA.</p>
            <p>
              I'm a mostly self taught software developer, and love to learn
              about new technologies and work on interesting projects that solve
              novel problems.
            </p>
            <p>
              On a professional level I create connected applications and
              experiences on the web. With my most recent position at
              Slickdeals, I expanded my skills as much as I could and sought out
              and took new challenges where presented. I got a taste of how
              larger organizations worked and the support and infrastructure it
              takes to run a website with millions of users, and I worked on
              amazing projects to push the standards of software engineering. I
              also got to work on a matured backend codebase and was able to
              grow as an engineer and tackle problems with a fullstack mindset
              and solve problems from end to end.
            </p>
            <p>Web technologies I've used:</p>
            <nuxt-content :document="content" />
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
export default {
  props: {
    content: {
      type: Object,
      default: () => {},
    },
  },
}
</script>
<style lang="scss" scoped>
figure.image {
  max-width: 350px;
  margin: 0 auto;
}
</style>
