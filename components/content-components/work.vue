<template>
  <section id="section-work" class="section">
    <div class="columns">
      <div class="column is-one-quarter">
        <div class="tabs">
          <ul>
            <li class="is-active" @click="changeTabs">
              <a>Pictures</a>
            </li>
            <li @click="changeTabs"><a>Music</a></li>
            <li @click="changeTabs"><a>Videos</a></li>
            <li @click="changeTabs"><a>Documents</a></li>
          </ul>
        </div>
      </div>
      <div class="column"></div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    changeTabs(event) {
      const tabs = document.querySelectorAll('#section-work div.tabs li')
      Array.prototype.forEach.call(tabs, function (tab) {
        tab.classList.remove('is-active')
      })
      event.target.parentNode.classList.add('is-active')
    },
  },
}
</script>

<style lang="scss" scoped>
.tabs {
  ul {
    border: none;
    flex-direction: column;
    li {
      @include standard-transition;
      width: 100%;
      display: flex;
      justify-content: flex-end;
      border-right: $link solid 2px;
      &:hover {
        border-right-color: $link-light;
      }
      &.is-active {
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
</style>
