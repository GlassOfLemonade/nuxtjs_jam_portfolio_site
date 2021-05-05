<template>
  <div class="tile is-parent" :class="width">
    <article class="tile is-child box">
      <div class="container">
        <figure v-for="icon in content.icons" :key="icon" class="image">
          <a
            v-if="icon === 'link'"
            :href="content.extlink"
            target="_blank"
            rel="noopener noreferrer"
          >
            <font-awesome-icon
              :icon="['fas', 'external-link-alt']"
              style="font-size: 1em;"
            />
          </a>
          <a
            v-else-if="icon === 'github'"
            :href="content.githublink"
            target="_blank"
            rel="noopener noreferrer"
          >
            <font-awesome-icon
              :icon="['fab', 'github']"
              style="font-size: 1em;"
            />
          </a>
        </figure>
      </div>
      <h3 class="title is-5">{{ content.title }}</h3>
      <div class="content">
        <nuxt-content :document="content" />
      </div>
    </article>
  </div>
</template>

<script>
export default {
  props: {
    width: {
      type: String,
      default: 'is-3',
    },
    content: {
      type: Object,
      default: () => {},
    },
  },
}
</script>

<style lang="scss">
#section-projects {
  article.box {
    div.container {
      display: flex;
      padding-bottom: 0.5rem;
    }
  }
  .nuxt-content ul {
    list-style-type: none;
    margin-left: 0;
    li {
      font-family: monospace;
      font-size: 0.75rem;
      color: $link;
    }
  }
  figure.image {
    padding: 0 4px;
    &:first-child {
      padding-left: 0;
    }
    &:last-child {
      padding-right: 0;
    }
  }
}
</style>
