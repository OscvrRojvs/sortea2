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
              <b-button
                pill
                variant="info"
                size="lg"
                @click="sorteo()"
                v-b-modal="'my-modal'"
              >Iniciar Sorteo</b-button>
              <b-modal id="my-modal">
                <h1>¡¡ {{win}} !!</h1>
              </b-modal>
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
  border: solid 3px rgb(190, 173, 58);
}
.input-group .comp {
  border: solid 3px rgb(190, 173, 58);
  border-radius: 10px 11px 11px 10px;
  padding-bottom: 5px;
}
.list-group .list-group-item {
  font-family: "Righteous", cursive;
  font-size: x-large;
  color: #083d77;
}
h1 {
  font-family: "Monoton", cursive;
  color: goldenrod;
  text-align: center;
  font-size: 7rem;
}
</style>
