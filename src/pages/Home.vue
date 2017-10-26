<template lang="html">
  <div class="home-page">
    <match-detail class="match-detail">
    </match-detail>
  </div>
</template>

<script>
  import MatchDetail from '@/components/MatchDetail'

  export default {
    components: {
      MatchDetail
    },

    data () {
      return {
        myName: 'Nghi'
      }
    }
  }
</script>

<style lang="css">
  .match-detail {
    width: 80%
  }

  .home-page {
    display: flex;
    justify-content: center;
  }
</style>
