<template>
  <section id="section-work" class="section">
    <div class="content"><h1 class="section-title">Work Experience</h1></div>
    <div class="columns work--wrapper">
      <div class="column is-one-quarter">
        <div class="tabs">
          <ul>
            <li
              v-for="(job, index) in content"
              :id="'tab-' + index"
              :key="index"
              :class="{ active: activeTab === index }"
              @click="changeTabs(index)"
            >
              <a>{{ job.title }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="column">
        <div
          v-for="(job, index) in content"
          :id="'content-' + index"
          :key="index"
          class="tab-content content"
          :class="{ active: activeTab === index }"
        >
          <h3 class="section-subtitle">{{ job.title }}</h3>
          <nuxt-content :document="content[index]" />
        </div>
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
  data: () => {
    return {
      activeTab: 0,
    }
  },
  methods: {
    changeTabs(index) {
      this.activeTab = index
    },
  },
}
</script>

<style lang="scss" scoped>
.container {
  max-width: 1040px;
}
.tab-content {
  display: none;
  &.active {
    display: flex;
    flex-direction: column;
  }
}
@media screen and (min-width: 769px) {
  .work--wrapper {
    min-height: 340px;
  }
  .tabs {
    ul {
      border: none;
      flex-direction: column;
      li {
        @include tile-transition;
        width: 100%;
        display: flex;
        justify-content: flex-end;
        border-right: $link solid 2px;
        &:hover {
          border-right-color: $link-light;
        }
        &.active {
          background: rgb(255, 255, 255);
          background: linear-gradient(
            90deg,
            rgba(255, 255, 255, 0) 20%,
            rgba(90, 219, 145, 0.35) 100%
          );
          border-right-color: $link-light;
          a {
            color: $link-light !important;
          }
        }
        a {
          border: none;
        }
      }
    }
  }
}
</style>
