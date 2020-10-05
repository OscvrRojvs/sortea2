<template>
  <div>
    <div id="premio">
      <h5>Premio:</h5>
      <input type="text" class="form-control" v-model="prem" placeholder="Ingrese un Premio" />
      <br>
      <h4>{{premio}}</h4>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      prem: ''
    }
  },
  computed: {
    premio () {
      return this.prem
    }
  }
}
</script>

<style scope>
#premio {
  width: 300px;
  margin-top: 30px;
  margin-left: 100px;
  margin-bottom: 10px;
}

#premio p {
  font-family: "Monoton", cursive;
  color: goldenrod;
  font-size: 2rem;
}

#premio input {
  border: solid 3px rgb(190, 173, 58);
}
h5 {
    font-family: 'Luckiest Guy', cursive;
    color: #083D77;
    font-size: xx-large;
}

h4 {
    font-family: 'Monoton', cursive;
    font-size: xx-large;
    color: goldenrod;
    text-align: center;
}
</style>
