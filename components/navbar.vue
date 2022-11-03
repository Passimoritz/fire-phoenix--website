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
        <b-tooltip target="avatar-login" triggers="hover" placement="auto" noninteractive>
          Einloggen | Registieren
        </b-tooltip>
        <b-avatar v-if="!loggedIn" id="avatar-login" icon="question-lg" to="/profiles/login" />
        <b-avatar v-else id="profile" :to="profiles[0].url" :src="profiles[0].path" />
        <b-tooltip target="profile" placement="auto" :title="profiles[0].name" />
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>

export default {
  props: {
    loggedIn: {
      type: Boolean,
      default: true
    }
  },
  data () {
    return {
      profiles: [
        {
          name: 'Passimoritz',
          path: 'https://placekitten.com/300/300',
          url: '/profiles/passimoritz'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
    .navbar {
        background-color: $color-primary;
        display: flex;
        flex-wrap: nowrap;
        width: 100%;

        .b-dropdown {
          background-color: $color-primary !important;
        }

        &-brand {
            color: $color-white !important;
        }

        .navbar-toggler {
          background-color: $color-white;
        }

        .nav-link {
            color: $color-white !important;
            transition: .33s;

            &:hover {
                color: $color-third !important;
            }
        }
    }
</style>
