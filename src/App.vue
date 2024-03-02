<script>
import Cartas from './components/Cartas.vue'
import Nav from './components/Nav.vue'
import Search from './components/Search.vue'

export default {
  name: 'App',
  components: {
    Cartas,
    Nav,
    Search
  },
  data() {
    return {
      
    }
  }
}
</script>

<template>
  <Nav></Nav>
  <Search></Search>

  <div id="contenedor">
    <div class="mx-auto container-fluid">
      <Cartas></Cartas>
    </div>
  </div>
</template>

<style scoped>
#contenedor {
  background-color: #f9f9f9;
}

button {
  margin-left: 0.3em;
} 
</style>
