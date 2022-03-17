<template>
  <div id="app">
    <Transition />
    <hr>
    <modal-aula></modal-aula>
  </div>
</template>

<script>
import Transition from './components/Transition.vue'
import ModalAula from './components/ModalAula.vue'

export default {
  name: 'App',
  components: {
    Transition,
    ModalAula
  }
}
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
