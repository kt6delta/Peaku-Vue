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
    <div id="cartas" class="card-body d-flex">
      <figure class="d-flex align-items-center me-4" style="width: 70px; height: auto;">
        <img :src="job.img" class="img-fluid" alt="...">
      </figure>
      <div class="card-text">
        <div class="d-flex">
          <h5 class="card-title me-3">{{ job.name }}</h5>
          <button type="button" class="me-1 btn btn-outline-secondary py-0 px-2 rounded-pill" v-for="(skill, index) in job.skills" :key="index">{{ skill }}</button>
        </div>
        <div class="d-flex align-items-end pt-3">
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.company }}</p>
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.place }}</p>
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.vacantes }}</p>
          <p class="me-5"><img src="#" class="img-fluid" alt="...">{{ job.day }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
#cartas p{
  font-size: 14.4px;
  font-family: 'Montserrat','Roboto','sans-serif';
  color: #212529;
}
#cartas button{
  font-size: 0.8em;
  color: #343a40!important;
  height: 21px!important;
}
#cartas{
  height: 102px;
}
</style>
