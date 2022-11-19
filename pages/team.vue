<template>
  <div class="team">
    <h2 class="heading">
      Unser Team
    </h2>
    <b-button-toolbar key-nav class="team__toolbar">
      <b-button-group>
        <b-button v-for="team in teams" :key="team" @click="showCardfromSelectedButton(team.text)">
          {{ team.text }}
        </b-button>
      </b-button-group>
    </b-button-toolbar>

    <b-card-group>
      <b-card class="team__card">
        <b-card-header>
          <b-card-title>{{ selectedTeam }}</b-card-title>
          <b-button @click="getUserfromTeam">Test </b-button>
        </b-card-header>
      </b-card>
    </b-card-group>
  </div>
</template>

<script>
export default {
  data () {
    return {
      selectedTeam: 'Administratoren',
      teams: [
        {
          text: 'Administratoren',
          users: [
            { username: 'Passimoritz', path: '', age: '21', job: 'Entwickler und Systemadministrator', other: '' },
            { username: 'Xrolix', path: '', age: '22', job: 'Teamleitung', other: '' }
          ]
        },
        {
          text: 'Supporter'
        },
        {
          text: 'Moderatoren'
        }
      ]
    }
  },
  head: {
    title: 'Team'
  },
  methods: {
    getUserfromTeam () {
      this.teams.forEach((team) => {
        if (team.text.includes(this.selectedTeam)) {
          console.log(team.users)
        }
      })
    },
    showCardfromSelectedButton (team) {
      this.selectedTeam = team
    }
  }
}
</script>

<style lang="scss">
  .team {

    &__toolbar {
      justify-content: center;

      .btn {
        margin-left: auto;
        background-color: $color-primary;
        transition: .33s;

        .active {
          background: rgba($color: #000000, $alpha: 1.0);
        }

        &:hover {
          background-color: $color-white;
          color: $color-primary;
        }
      }
    }

    &__card {
      margin-top: 40px;
      text-align: center;
    }

    .heading {
      text-align: center;
      margin-bottom: 20px;
    }
  }
</style>
