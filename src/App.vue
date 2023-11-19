<script>
  import Header from "./components/Header.vue"
  import Card from "./components/Card.vue"
  import initialCards from "./initialCards"

  export default {
    data () {
      return {
        cards : {
          backlog: initialCards.backlog,
          dev: initialCards.dev,
          testes: initialCards.testes,
          fechados: []
        }
      }
    },
  }
  
</script>

<template>
  <Header />
  <div class="board">
    <div class="lane">
      <h2 class="lane-title">Backlog</h2>
      <Card v-for="card in cards.backlog" :key="card.id">{{ card.text }}</Card>
    </div>
    <div class="lane">
      <h2 class="lane-title">Desenvolvimento</h2>
      <Card v-for="card in cards.dev" :key="card.id">{{ card.text }}</Card>
    </div>
    <div class="lane">
      <h2 class="lane-title">Testes</h2>
      <Card v-for="card in cards.testes" :key="card.id">{{ card.text }}</Card>
    </div>
    <div class="lane">
      <h2 class="lane-title">Fechados</h2>
      <Card v-for="card in cards.fechados" :key="card.id">{{ card.text }}</Card>
    </div>
  </div>
</template>

<style scoped>
.board{
  display: flex;
  justify-content: flex-start;
}
.lane{
  background: var(--color-gray);
  width: 23rem;
  height: 30rem;
  border-radius: 0.8rem;
  box-shadow: 0 0.1rem 0.2rem 0 rgba(33, 33, 33, 0.1);
  margin: 0.8rem;
}
.lane-title{
  margin-bottom: 0.6rem;
  padding: 0.8rem 0.5rem;
}
</style>
