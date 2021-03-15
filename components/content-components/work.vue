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
                    Web Developer at
                    <a
                      href="https://www.causeforce.com/"
                      rel="noopener"
                      target="_blank"
                    >
                      CauseForce
                    </a>
                  </h2>
                </div>
                <div class="body">
                  <span class="section-subtitle">Aug 2019 - Dec 2020</span>
                  <ul>
                    <li>
                      Built websites and developed web content to client
                      specifications on Luminate Online and Rallybound.
                      Developed documentation and testing methodology to ensure
                      cross-browser compatibility and responsiveness.
                    </li>
                    <li>
                      Leveraged third party and platform APIs to develop web
                      applications with interactive and personalized content.
                    </li>
                    <li>
                      Led project to rebrand, modernize, and rebuild our
                      corporate website, utilizing modern frameworks such as
                      VueJS and Tailwind CSS.
                    </li>
                    <li>
                      Maintained, refactored, and updated code as necessary to
                      keep apps connected through APIs running and error-free,
                      with such projects utilizing a variety of languages,
                      frameworks, and platforms, such as Typescript, AngularJS,
                      Heroku, and AWS.
                    </li>
                    <li>
                      Worked and communicated with multi-disciplinary teams with
                      modern project management standards (Agile/Scrum-like),
                      with our tool of choice Asana.
                    </li>
                    <li>
                      Wrote, maintained, and updated technical documentation
                      (wiki-style) on projects of non-trivial complexity.
                    </li>
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
                    IT Manager &amp; Analyst at
                    <a
                      href="https://hallmarkfloors.com/"
                      rel="noopener"
                      target="_blank"
                    >
                      Hallmark Floors
                    </a>
                  </h2>
                </div>
                <div class="body">
                  <span class="section-subtitle">Oct 2014 - Aug 2019</span>
                  <ul>
                    <li>
                      Led project to migrate the firm’s operations from
                      QuickBooks to NetSuite in order to meet growing demands
                      for operational efficiency and inventory tracking.
                      Administrated NetSuite thereafter on a variety of tasks
                      including: General user administration, setting up reports
                      and dashboards, and developing UI customizations and
                      custom data solutions through the use of Javascript and
                      NetSuite’s API.
                    </li>
                    <li>
                      Windows Server 2012 basic administration regarding active
                      directory and network drives, worked with and managed
                      contracts with external IT services where needed.
                    </li>
                    <li>
                      Microsoft Excel reporting (Pivot Tables, VBA development
                      for automated data querying and sorting, data
                      visualization)
                    </li>
                    <li>
                      Managed Wordpress website and supported projects on
                      managed server hosting (cPanel).
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
