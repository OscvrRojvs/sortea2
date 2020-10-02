<template>
  <div id="app">
    <b-container>
      <b-row>
        <b-col>
          <Header></Header>
        </b-col>
        <b-col>
          <Premio></Premio>
        </b-col>
      </b-row>
    </b-container><hr>
    <Participantes></Participantes>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Participantes from './components/Participantes.vue'
import Premio from './components/Premio.vue'

export default {
  name: 'App',
  components: {
    Header,
    Participantes,
    Premio
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 5px;
}
</style>
