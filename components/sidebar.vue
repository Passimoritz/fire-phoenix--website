<template>
  <div class="sidebar">
    <div class="sidebar__wrapper">
      <b-button to="/forum">
        <b-icon icon="house-fill" />
        <span class="link-text">Startseite</span>
      </b-button>
      <b-button to="/forum/categories">
        <b-icon icon="card-list" />
        <span class="link-text">Kategorien</span>
      </b-button>
      <b-button to="/forum/users">
        <b-icon icon="person-fill" />
        <span class="link-text">Benutzer</span>
      </b-button>
    </div>
  </div>
</template>

<style lang="scss">
.sidebar {
  background-color: $color-blue;
  display: flex;
  flex-direction: column;
  height: 100vh;
  justify-content: center;
  top: 0;
  left: 0;
  position: fixed;
  width: 180px;
  box-shadow: 6px 0 5px -5px $color-grey;

  &__wrapper {
    .btn {
      background-color: $color-grey;
      padding-left: 20px;
      font-size: 18px;
      text-align: left;
      margin-top: 3px;
      width: 100%;
    }

    .nuxt-link-exact-active {
        background-color: $color-white;
        color: $color-blue;
    }

    .b-icon {
      margin-right: 10px;
    }
  }
}

@media screen and (max-width: 991px) {
  .sidebar {
    width: 60px;
  }
  .link-text {
      display: none;
  }
}
</style>
