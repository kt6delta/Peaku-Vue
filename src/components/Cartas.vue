<script>
export default {
  name: 'Cartas',
  props: ['Propmsg'],
  data() {
    return {
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
  {{ Propmsg }}
  <li v-for="(job, indice) in jobs" :key="indice"> {{ job }} </li>
  
</template>

<style scoped></style>
