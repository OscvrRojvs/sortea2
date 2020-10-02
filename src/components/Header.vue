<template>
  <div>
    <header>
      <div class="jumbotron">
        <h1 class="display-4">{{title}}</h1>
        <p class="lead">LA NUEVA FORMA DE REALIZAR SORTEOS</p>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'SORTEA2'
    }
  }
}
</script>

<style scoped>
.jumbotron {
    background-color: white;
    height: 180px;
}

.jumbotron h1 {
    font-family: 'Monoton', cursive;
    font-size: 3rem;
    color: goldenrod;
}

.jumbotron p {
    font-family: 'Luckiest Guy', cursive;
    font-size: 2rem;
    color: #083D77;
}
</style>
