<template>
  <header class="header">
    <nav
      class="navbar is-fixed-top"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
          <img
            src="https://bulma.io/images/bulma-logo.png"
            width="112"
            height="28"
          />
        </a>

        <a
          role="button"
          class="navbar-burger burger"
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
export default {}
</script>

<style lang="scss" scoped>
nav {
  padding: 0.5rem 1rem;
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
</style>
