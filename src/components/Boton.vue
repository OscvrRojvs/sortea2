<template>

</template>

<script>
export default {
  props: ['competidores'],
  data () {
    return {
      ind: '',
      win: ''
    }
  },
  methods: {
    sorteo () {
      this.ind = Math.floor(Math.random() * this.competidores.length)
      this.win = this.competidores[this.ind].nombre
    }
  }
}
</script>
