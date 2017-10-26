<template lang="html">
  <img src="{{logo}}">
  <i>{{teamName}}</i>
</template>

<script>
export default {
  props: {
    team: {
      required: true
    }
  },

  computed: {
    teamName: () => {
      return this.team.name
    },
    logo: () => {
      return this.team.logo
    }
  }

}
</script>
  
<style lang="css">
</style>
