<template>
    <b-breadcrumb :items="teams" />
</template>

<script>
export default {
  props: {
  },
  head: {
    title: 'Team'
  },
  data () {
    return {
      teams: [
        {
          text: 'Supporter',
          to: '/team/supporter'
        },
        {
          text: 'Moderatoren',
          to: '/team/moderators'
        },
        {
          text: 'Administratoren',
          to: '/team/'
        }
      ]
    }
  }
}
</script>

<style>

    .card {
        width: 30%;
        margin: 0 auto;
    }

    .team {
        text-align: center;
    }
</style>
