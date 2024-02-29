<script>
import Cartas from './components/Cartas.vue'
export default {
  name: 'App',
  components: {
    Cartas
  },
  data() {
    return {
      msg: "holi",
      jobs: [
        {
          name: "job 1",
          company: "company 1"
        },
        {
          name: "job 2",
          company: "company 2"
        }
      ]
    }
  }
}
</script>

<template>
  <Cartas :Propmsg="msg"></Cartas>
</template>

<style >

</style>
