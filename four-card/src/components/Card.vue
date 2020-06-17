<template>
  <div class="card" :class="cardData.cardType">
    <h1>{{ cardData.head }}</h1>
    <p>{{ cardData.text }}</p>
    <img class="card-img" :src="cardData.image">
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: ['cardData', 'background', 'linkColor', 'hoverBackground']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.card {
  border-top: 5px solid;
  display: flex;
  flex-direction: column;
  text-align: left;
  background-color: white;
  border-radius: 5px;
  box-shadow: 1px 1px 10px 0px rgba(204,204,204,0.5);
  width: 350px;
  padding: 25px;
  margin: 25px;
  h1 {
    font-size: 20px;
    font-weight: 600;
    color: hsl(234, 12%, 34%);
  }
  p {
    font-weight: 400;
    color: hsl(229, 6%, 66%);
  }
  .card-img {
    align-self: flex-end;
    width: 70px;
    height: 70px;
  }
  &.red {
    border-top-color: hsl(0, 78%, 62%);
  }
  &.blue {
    border-top-color: hsl(212, 86%, 64%);
  }
  &.yellow {
    border-top-color: hsl(34, 97%, 64%);
  }
  &.cyan {
    border-top-color: hsl(180, 62%, 55%);
  }
}
</style>
