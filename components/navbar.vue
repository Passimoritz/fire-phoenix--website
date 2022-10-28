<template>
  <b-navbar toggleable="lg" fixed="top">
    <b-nav-toggle target="nav-collapse" />
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-brand>Fire-Phoenix.</b-navbar-brand>
      <b-navbar-nav class="ml-5">
        <b-nav-item to="/">
          Startseite
        </b-nav-item>
        <b-nav-item to="/team">
          Team
        </b-nav-item>
        <b-nav-item to="/projects">
          Projekte
        </b-nav-item>
        <b-nav-item to="/news">
          News
        </b-nav-item>
        <b-nav-item to="/forum">
          Forum
        </b-nav-item>
      </b-navbar-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item to="/profiles/login">
          Einloggen
        </b-nav-item>
        <b-nav-item to="/profiles/register">
          Registrieren
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
</script>

<style lang="scss">
    .navbar {
        background-color: $color-blue;
        display: flex;
        flex-wrap: nowrap;
        width: 100%;

        &-brand {
            color: white !important;
        }

        .nav-link {
            color: $color-white !important;
            transition: .33s;

            &:hover {
                color: $color-turquoise !important;
            }
        }
    }
</style>
