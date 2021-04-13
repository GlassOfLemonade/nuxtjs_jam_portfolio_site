<template>
  <header class="header">
    <nav
      class="navbar is-fixed-top"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a class="navbar-item logo" href="/">
          <object
            id="site-logo"
            data="~assets/kevint-logo.svg"
            type="image/svg+xml"
          >
            <img src="~assets/kevint-logo.svg" />
          </object>
        </a>

        <a
          role="button"
          class="navbar-burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navbar"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navbar" class="navbar-menu">
        <div class="navbar-end">
          <a href="#section-about" class="navbar-item">About Me</a>

          <a href="#section-work" class="navbar-item">Experience</a>

          <a href="#section-projects" class="navbar-item">Projects</a>

          <a href="#section-contact" class="navbar-item">Contact Me</a>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  mounted() {
    this.burgerEventHandler()
  },
  methods: {
    burgerEventHandler() {
      const _burgerMenus = Array.prototype.slice.call(
        document.querySelectorAll('.navbar-burger')
      )
      if (_burgerMenus.length > 0) {
        _burgerMenus.forEach((element) => {
          element.addEventListener('click', () => {
            const target = element.dataset.target
            const _target = document.getElementById(target)

            element.classList.toggle('is-active')
            _target.classList.toggle('is-active')
          })
        })
      }
    },
  },
}
</script>

<style lang="scss" scoped>
nav {
  padding: 1rem 1.5rem;
  .logo {
    padding: 0 !important;
    #site-logo {
      width: 3.5rem;
      img {
        max-height: 3.5rem;
      }
    }
  }
  .navbar-burger {
    > span:first-child,
    > span:last-child {
      transition: 0.3s;
    }
  }
  .navbar-end {
    a.navbar-item {
      border-radius: 0.35rem;
      background: $primary-dark;
      margin: 0.5rem;
      @include tile-transition;
      &:hover {
        box-shadow: 0rem 0.25em 1.5rem -0.25rem rgba(10, 10, 10, 0.3);
      }
    }
  }
}
</style>
