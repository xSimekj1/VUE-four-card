<template>
  <div id="app">
    <div class="intro">
      <h1>Reliable, efficient delivery</h1>
      <h1 class="main">Powered by Technology</h1>
      <p>Our Artificial Intelligence powered tools use millions of project data points to ensure that your project is successful</p>
    </div>
    <div class="card-holder">
      <div class="col">
        <Card :card-data="cardData[3]"/>
      </div>
      <div class="col">
        <Card :card-data="cardData[0]"/>
        <Card :card-data="cardData[2]"/>
      </div>
      <div class="col">
        <Card :card-data="cardData[1]"/>
      </div>
    </div>
  </div>
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  data: () => ({
    cardData: [
      {
        head: 'Team Builder',
        text: 'Scans our talent network to create the optimal team for your project',
        cardType: 'red',
        image: require('./assets/icon-team-builder.svg')
      },
      {
        head: 'Calculator',
        text: 'Uses data from past projects to provide better delivery estimates',
        cardType: 'blue',
        image: require('./assets/icon-calculator.svg')
      },
      {
        head: 'Karma',
        text: 'Regularly evaluates our talents to ensure quality',
        cardType: 'yellow',
        image: require('./assets/icon-karma.svg')
      },
      {
        head: 'Supervisor',
        text: 'Monitors activity to identify project roadblocks',
        cardType: 'cyan',
        image: require('./assets/icon-supervisor.svg')
      }
    ]
  })
}
</script>

<style lang="scss">
  #app {
    display: flex;
    align-items: center;
    flex-direction: column;
  }
  .intro {
    justify-content: center;
    text-align: center;
    margin-top: 25px;
    width: 500px;
    h1 {
      margin: 0;
      font-size: 2rem;
      font-weight: 200;
      color: hsl(229, 6%, 66%);
      &.main {
        font-weight: 600;
        color: hsl(234, 12%, 34%);
      }
    }
    p {
      color: hsl(229, 6%, 66%);

    }
  }
  .card-holder {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
  }
  .row {
    display: flex;
    flex-direction: row;
  }
  .col {
    display: flex;
    flex-direction: column;
  }
</style>
