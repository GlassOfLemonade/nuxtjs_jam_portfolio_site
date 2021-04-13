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
          <a href="#section-about" class="navbar-item navbar-item-1">
            About Me
          </a>

          <a href="#section-work" class="navbar-item navbar-item-2">
            Experience
          </a>

          <a href="#section-projects" class="navbar-item navbar-item-3">
            Projects
          </a>

          <a href="#section-contact" class="navbar-item navbar-item-4">
            Contact Me
          </a>
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
@include keyframe(menuAnim) {
  0% {
    opacity: 0;
    transform: rotateX(-90deg);
  }
  50% {
    transform: rotateX(-20deg);
  }
  100% {
    opacity: 1;
    transform: rotateX(0deg);
  }
}

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
  div.navbar-menu {
    .navbar-end {
      a.navbar-item {
        border-radius: 0.35rem;
        background: $primary-dark;
        margin: 0.5rem;
        @include tile-transition;
        &:hover {
          box-shadow: 0rem 0.25em 1.5rem -0.25rem rgba(10, 10, 10, 0.3);
        }
        @media screen and (max-width: 1023px) {
          display: none;
          opacity: 0;
        }
      }
    }
    &.is-active {
      > .navbar-end {
        > a.navbar-item {
          @media screen and (max-width: 1023px) {
            display: block;
          }
        }
        @for $num from 1 through 4 {
          a.navbar-item-#{$num} {
            // animation: menuAnim 300ms ($num * 60ms) ease-in-out forwards;
            @include animation(
              menuAnim,
              300ms,
              ($num * 60ms),
              ease-in-out,
              forwards
            );
            transform-origin: top center;
          }
        }
      }
    }
  }
}
</style>
