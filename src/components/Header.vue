<template>
  <div>
    <header>
      <div class="jumbo">
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
.jumbo {
    background-color: white;
    height: 180px;
    margin-top: 20px;
}

.jumbo h1 {
    font-family: 'Monoton', cursive;
    font-size: 4rem;
    color: goldenrod;
}

.jumbo p {
    font-family: 'Luckiest Guy', cursive;
    font-size: 2rem;
    color: #083D77;
}
</style>
