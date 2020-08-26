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
          data-target="navbarBasicExample"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navbarBasicExample" class="navbar-menu">
        <div class="navbar-end">
          <a href="#section-about" class="navbar-item">About Me</a>

          <a href="#" class="navbar-item">Experience</a>

          <a href="#" class="navbar-item">Projects</a>

          <a href="#" class="navbar-item">Contact Me</a>
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
  padding: 0 1rem;
}

a.navbar-item {
  &:hover {
    @include standard-transition;
    box-shadow: 0rem 0.25em 1.5rem -0.25rem rgba(10, 10, 10, 0.3);
  }
}
</style>
