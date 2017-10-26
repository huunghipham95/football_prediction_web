<template lang="html">
  <div class="">
    <match-additional-infor class="match-info"></match-additional-infor>
    <div class="match-detail-container">
      <div class="match-score-container">
        <div class="team-container">
          <img :src="homeLogo" class="team-logo">
          <span class="c-white text-padding-left">{{homeTeam.name}}</span>
        </div>
        <div class="match-score">
          <span class="score">{{homeTeam.goals}}    -    {{awayTeam.goals}}</span>
        </div>
        <div class="team-container align-end">
          <span class="c-white text-padding-right">{{awayTeam.name}}</span>
          <img :src="awayLogo" class="team-logo">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MatchAdditionalInfor from '@/components/MatchAdditionalInfor'

export default {
  components: {
    MatchAdditionalInfor
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
    justify-content: center;
    background-image: url('../assets/EPL.png');
  }
  .team-container {
    width: 45%;
    display: flex;
    align-items: center;
  }
  .match-score {
    background-color: #e90052;
    height: 60px;
    width: 10%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
  }
  .align-end {
    justify-content: end;
  }
  .team-logo {
    height: 60px;
    width: 60px;
    background-color: white;
  }
  .c-white {
    color: white;
    font-weight: bold;
    font-size: 20px;
  }
  .score {
    font-size: 35px;
    font-weight: bold;
  }
  .match-info {
    margin-top: 10px;
  }
  .match-score-container {
    display: flex;
    align-items: center;
    background-color: #38003c;
    width: 80%;
    margin-top: 200px;
  }
  .text-padding-left {
    padding-left: 25px;
  }
  .text-padding-right {
    padding-right: 25px;
  }
</style>
