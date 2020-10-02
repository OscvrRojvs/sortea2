<template>
  <div>
    <div id="premio">
      <input type="text" class="form-control" v-model="prem" placeholder="Ingrese un Premio" />
      <h5>Premio:</h5>
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
  margin-left: 100px;
  margin-bottom: 10px;
}

#premio p {
  font-family: "Monoton", cursive;
  color: goldenrod;
  font-size: 2rem;
}

#premio input {
  border-radius: 10px 11px 11px 10px;
}
h5 {
    font-family: 'Luckiest Guy', cursive;
    color: #083D77;
    font-size: xx-large;
}

h4 {
    font-family: 'Monoton', cursive;
    color: goldenrod;
    text-align: center;
    font-size: 6rem;

}
</style>
