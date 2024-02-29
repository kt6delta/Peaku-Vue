<script>
export default {
  name: 'Cartas',
  props: ['Propmsg'],
  data() {
    return {
      jobs: [
        {
          name: "job 1",
          img: "https://via.placeholder.com/150",
          company: "company 1",
          place:"place 1",
          salario:"confidencial",
          vacantes: "2",
          day: "hoy",
          skills: ["skill 1", "skill 2", "skill 3"]
        },
        {
          name: "job 2",
          img: "https://via.placeholder.com/150",
          company: "company 2",
          place:"place 2",
          vacantes: "3",
          day: "ayer",
          salario:"confidencial",
          skills: ["skill 1", "skill 2", "skill 3"]
        }
      ]
    }
  }
}
</script>

<template>
  {{ Propmsg }}
  <div class="card m-3" v-for="(job, indice) in jobs" :key="indice">
    <div class="card-body d-flex">
      <figure class="d-flex align-items-center" style="width: 100px; height: auto;">
        <img :src="job.img" class="img-fluid" alt="...">
      </figure>
      <h5 class="card-title me-2">{{ job.name }}</h5>
      <div class="card-text">
        <div class="d-flex">
          <p class="border me-2" v-for="(skill, index) in job.skills" :key="index">{{ skill }}</p>
        </div>
        <div class="d-flex">
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.company }}</p>
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.place }}</p>
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.vacantes }}</p>
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.day }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
