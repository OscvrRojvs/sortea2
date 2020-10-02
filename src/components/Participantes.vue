<template>
  <div>
    <div id="box1">
      <b-container class="bv-example-row">
        <b-row>
          <b-col>
            <section class="input-group input-group-lg">
              <input
                class="comp form-control"
                type="text"
                v-model="newCom"
                @keyup.enter="addCom"
                placeholder="Ingrese un Participante"
              />
            </section>
            <ol class="list-group list-group-flush">
              <li
                class="list-group-item list-group-item-action"
                v-for="competidor in competidores"
                :key="competidor.id"
              >{{competidor.nombre}}</li>
            </ol>
          </b-col>
          <b-col>
            <div id="button">
              <button
                type="button"
                @click="sorteo()"
                class="btn btn-secondary btn-dark btn-lg"
                v-b-modal="'my-modal'"
              >Iniciar Sorteo</button>
              <b-modal id="my-modal"><h1>{{win}}</h1></b-modal>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      competidores: [{ nombre: '' }],
      newCom: '',
      ind: '',
      win: ''
    }
  },
  methods: {
    addCom () {
      this.competidores.push({
        nombre: this.newCom
      })
      this.newCom = ''
    },
    sorteo () {
      this.ind = Math.floor(Math.random() * this.competidores.length)
      this.win = this.competidores[this.ind].nombre
    }
  }
}
</script>

<style scope>
.input-group input {
  border: solid 3px rgb(129, 122, 78);
}
.input-group .comp {
  border: solid 3px rgb(129, 122, 78);
  border-radius: 10px 11px 11px 10px;
  box-shadow: -7px 10px 16px -8px rgba(236, 167, 44, 1);
  padding-bottom: 5px;
}
.list-group .list-group-item {
  font-family: "Righteous", cursive;
  font-size: x-large;
}
h1{
  font-family: 'Monoton', cursive;
    color: goldenrod;
    text-align: center;
    font-size: 4rem;
}
</style>
