<template>
  <div>
    <Header></Header>
    <Banner></Banner>
    <Benefit></Benefit>
    <Service></Service>
    <Game></Game>
    <Custom></Custom>
    <Footer></Footer>
  </div>
</template>

<script>
import Benefit from "../components/Benefit.vue";
import Game from "../components/Game.vue";
import Footer from "../components/Footer.vue";
export default {
    name: "IndexPage",
    components: { Benefit, Game, Footer }
}
</script>

<style>
  body {
    background-color: #0E0E0E;
  }
</style>
