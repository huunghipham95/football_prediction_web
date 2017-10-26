<template lang="html">
  <div class="">
    <league-header></league-header>
    <div class="match-detail-container">
      <div class="team-container">
        <span class="c-white">{{homeTeam.name}}</span>
        <img :src="homeLogo" class="team-logo">
      </div>
      <div class="match-score">
        <span class="score">{{homeTeam.goals}}    -    {{awayTeam.goals}}</span>
      </div>
      <div class="team-container">
        <img :src="awayLogo" class="team-logo">
        <span class="c-white">{{awayTeam.name}}</span>
      </div>
    </div>
  </div>
</template>

<script>
import LeagueHeader from '@/components/LeagueHeader'

export default {
  components: {
    LeagueHeader
  },

  props: {
    homeTeam: {
      required: false,
      default: () => {
        return {
          name: 'Manchester United',
          logo: 'static/images/mu_logo.png',
          goals: 5
        }
      }
    },
    awayTeam: {
      required: false,
      default: () => {
        return {
          name: 'Manchester City',
          logo: 'static/images/mc_logo.png',
          goals: 3
        }
      }
    }
  },

  computed: {
    homeLogo () {
      return this.homeTeam.logo
    },
    awayLogo () {
      return this.awayTeam.logo
    }
  }
}
</script>

<style lang="css">
  .match-detail-container {
    display: flex;
    align-items: center;
    background-image: url('../assets/EPL.png');
  }
  .team-container {
    height: 150px;
    width: 38%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
  }
  .match-score {
    background-color: white;
    height: 50px;
    border-radius: 10px;
    width: 24%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .team-logo {
    height: 80px;
    width: 80px;
  }
  .c-white {
    color: white;
  }
  .score {
    font-size: 30px;
    font-weight: bold;
  }
</style>
