<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Card
    :card-data="cardData[0]"
    />
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
        text: 'Lorem ipsum',
        cardType: 'red-house'
      },
      {
        head: 'Calculator',
        text: 'Lorem ipsum',
        cardType: 'blue-machine'
      },
      {
        head: 'Karma',
        text: 'Lorem ipsum',
        cardType: 'yellow-light'
      },
      {
        head: 'Supervisor',
        text: 'Lorem ipsum',
        cardType: 'cyan-glass'
      }
    ]
  })
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
