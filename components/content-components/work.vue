<template>
  <section id="section-work" class="section">
    <div class="desktop">
      <div class="content"><h1 class="section-title">Work Experience</h1></div>
      <!-- Save columns for a later design -->
      <!-- <div class="columns">
        <div class="column is-one-quarter">
          <div class="tabs">
            <ul>
              <li class="is-active" @click="changeTabs(0)">
                <a>CauseForce</a>
              </li>
              <li @click="changeTabs(1)"><a>Hallmark Floors</a></li>
            </ul>
          </div>
        </div>
        <div class="column">
          <div class="tab-content content is-active">
            <h3 class="section-subtitle">CauseForce</h3>
          </div>
          <div class="tab-content content">
            <h3 class="section-subtitle">Hallmark Floors</h3>
          </div>
        </div>
      </div> -->
      <!-- Use tiles for a straightforward design-->
      <div class="container">
        <div class="tile is-ancestor">
          <div class="tile is-parent is-12">
            <div class="tile is-child box">
              <div class="content">
                <div class="headings">
                  <h2>
                    Position at
                    <a
                      href="https://www.google.com/"
                      rel="noopener"
                      target="_blank"
                    >
                      Company
                    </a>
                  </h2>
                </div>
                <div class="body">
                  <span class="section-subtitle">Date - Date</span>
                  <ul>
                    <li>
                      Nam eget ligula tincidunt, aliquam felis molestie,
                      pharetra lacus.
                    </li>
                    <li>Praesent scelerisque orci eu tristique tristique.</li>
                    <li>Maecenas tempus ipsum ac dignissim faucibus.</li>
                    <li>Sed ultricies diam a enim interdum pharetra.</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="tile is-ancestor">
          <div class="tile is-parent is-12">
            <div class="tile is-child box">
              <div class="content">
                <div class="headings">
                  <h2>
                    Position at
                    <a
                      href="https://www.google.com/"
                      rel="noopener"
                      target="_blank"
                    >
                      Company
                    </a>
                  </h2>
                </div>
                <div class="body">
                  <span class="section-subtitle">Date - Date</span>
                  <ul>
                    <li>
                      Aliquam semper urna mauris, non pellentesque leo ornare
                      at. Lorem ipsum dolor sit amet, consectetur adipiscing
                      elit. Aliquam sit amet egestas metus, vel sodales odio.
                      Vestibulum augue ante, euismod vel feugiat sit amet,
                      venenatis suscipit lorem. Etiam vitae ultricies massa, sed
                      pulvinar sem.
                    </li>
                    <li>
                      Phasellus bibendum tempor neque sit amet tincidunt. Ut
                      cursus, risus vel consectetur ultricies, dui orci
                      tincidunt nibh, et rutrum mauris tortor pellentesque
                      ligula. Aenean eget purus posuere nisi porta ultrices eget
                      ut orci. In hac habitasse platea dictumst.
                    </li>
                    <li>
                      Suspendisse tincidunt et ligula a feugiat. Aliquam erat
                      volutpat. Nulla facilisi. Nam tempor posuere massa, sed
                      feugiat justo consequat vel.
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    changeTabs(index) {
      const tabs = document.querySelectorAll('#section-work div.tabs li')
      const content = document.querySelectorAll('#section-work div.tab-content')
      Array.prototype.forEach.call(tabs, function (tab) {
        tab.classList.remove('is-active')
      })
      Array.prototype.forEach.call(content, function (c) {
        c.classList.remove('is-active')
      })
      // add 'is-active' to appropriate elements
      event.target.parentNode.classList.add('is-active')
      content[index].classList.add('is-active')
    },
  },
}
</script>

<style lang="scss" scoped>
.container {
  max-width: 1040px;
}
@media screen and (min-width: 1040px) {
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
  .tab-content {
    display: none;
    &.is-active {
      display: flex;
    }
  }
}
</style>
