<template>
  <div class="purple-blur-background">
    <link rel="stylesheet" href="static/font-awesome/css/font-awesome.min.css">
    <span class="text-white">
      {{info.date}}
      <a class="fa fa-address-card text-padding-left"></a>
      {{info.referee}}
      <a class="fa fa-university text-padding-left"></a>
      {{info.stadium}}
      <a class="text-padding-left">Att: {{info.attendence}}</a>
    </span>
  </div>
</template>

<script>
  export default {
    props: {
      info: {
        default: () => {
          return {
            date: 'Sat 30 Sep 2017',
            referee: 'Mike Dean',
            stadium: 'Old Trafford',
            attendence: 74562
          }
        }
      }
    }
  }
</script>

<style scoped>
  .purple-blur-background {
    background-color: rgba(56, 0, 60, 0.9);
    padding-top: 5px;
    padding-bottom: 5px;
  }

  .text-white {
    color: white;
    padding-left: 20px;
    font-size: 12px;
  }

  .text-padding-left {
    padding-left: 10px;
  }

</style>