<script>
export default {
  name: 'Cartas',
  data() {
    return {
      ver: [],
      jobs: [
        {
          name: "Analista de Datos",
          img: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/48484/skalo.jpg",
          company: "Skalo",
          tipo: "Remoto",
          vacantes: "1",
          day: "2",
          salario: true,
          salario_1: 5500000,
          salario_2: 6500000,
          salario_3: "$ 5.5M - 6.5M COP",
          skills: ["skill 1", "skill 2", "skill 3"],
          see_description: false,
          description: "A partir de la base de datos de las contrapartes, se requiere porponer una solución que permita la visualización del comportamiento de los datos con enfoque en riesgos."
        },
        {
          name: "Coordinador de Tecnología Educativa",
          img: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/530708/Logo-Genuine-Digital-School.jpg",
          company: "Genuine Digital School",
          salario: false,
          salario_1: 3500000,
          salario_2: 4000000,
          salario_3: "$ 3.5M - 4M COP",
          tipo: "Remoto",
          vacantes: "3",
          day: "2",
          skills: ["skill 1", "skill 2", "skill 3"],
          see_description: false,
          description: "Capaz de identifcar necesidades y promover las actividades con pedagogía adecuada."
        },
        {
          name: "Coordinadora de Gestión Humana",
          img: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/530708/Logo-Genuine-Digital-School.jpg",
          company: "Genuine Digital School",
          salario: true,
          salario_1: 3000000,
          salario_2: 4000000,
          salario_3: "$ 3M - 4M COP",
          tipo: "Remoto",
          vacantes: "1",
          day: "7",
          skills: ["skill 1", "skill 2", "skill 3"],
          see_description: false,
          description: "Manejo de un personal que cuenta con 80 administrativos y 260 de tienda."
        },
        {
          name: "Ejecutivo Comercial en Ciberseguridad",
          img: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/465677/acg.png",
          company: "Advisor Consulting Group",
          salario: false,
          salario_1: 9000000,
          salario_2: 10000000,
          salario_3: "$ 9M - 10M COP",
          tipo: "Bogotá",
          vacantes: "1",
          day: "3",
          skills: ["skill 1", "skill 2", "skill 3"],
          see_description: false,
          description: "Con mínimo 5 años de experiencia liderando proyectos de Ciberseguridad."
        },
        {
          name: "Desarrollador Senior Java EE",
          img: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/80639/Invoway.png",
          company: "INVOWAY",
          salario: true,
          salario_1: 4000000,
          salario_2: 6300000,
          salario_3: "$ 4M - 6.3M COP",
          tipo: "Remoto en Colombia",
          vacantes: "5",
          day: "2",
          skills: ["skill 1", "skill 2", "skill 3"],
          see_description: false,
          description: "Con 4 años de experiencia en la herramienta y capacidad de innovación."
        }
      ]
    }
  },
  onMounted() {
    this.ver = this.jobs.map(() => false);
  },
  methods: {
    verMas(indice) {
      this.ver[indice] = !this.ver[indice]
      this.jobs[indice].see_description = !this.jobs[indice].see_description
    },
    convertirADinero(value) {
      return new Intl.NumberFormat("es-CO", { style: "currency", "currency": "COP", notation: "compact", compactDisplay: "short", }).format(value);
    },
  },
}
</script>

<template>

  <!-- Recorrido de trabajos. -->
  <div class="card m-3" v-for="(job, indice) in jobs" :key="indice">
    <div id="cartas" class="card-body d-flex" @click="verMas(indice)">
      <div class="d-flex">

        <!-- Imagen. -->
        <figure class="d-flex align-items-center m-0 me-4" style="width: 100px; height: auto;">
          <img :src="job.img" class="img-fluid" alt="...">
        </figure>

        <!-- Cuerpo. -->
        <div class="card-text">

          <!-- Título. -->
          <div class="d-flex">
            <h5 class="card-title bold pl-md-2 pr-md-2 mb-0 pb-0">{{ job.name }}</h5>&nbsp;&nbsp;&nbsp;
            <button disabled type="button" class="me-1 btn btn-outline-secondary py-0 px-2 rounded-pill"
              v-for="(skill, index) in job.skills" :key="index">{{ skill }}</button>
          </div>

          <!-- Generales. -->
          <div v-show="!ver[indice]" style="width: 80vw;">
            <div class="d-flex align-items-end pt-3">

              <p class="me-5 d-flex">
                <span class="me-1 pb-2"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em"
                    focusable="false" role="img" aria-label="building" xmlns="http://www.w3.org/2000/svg"
                    fill="currentColor" class="bi-building b-icon bi">
                    <g data-v-378c8849="">
                      <path fill-rule="evenodd"
                        d="M14.763.075A.5.5 0 0 1 15 .5v15a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5V14h-1v1.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V10a.5.5 0 0 1 .342-.474L6 7.64V4.5a.5.5 0 0 1 .276-.447l8-4a.5.5 0 0 1 .487.022zM6 8.694 1 10.36V15h5V8.694zM7 15h2v-1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5V15h2V1.309l-7 3.5V15z">
                      </path>
                      <path
                        d="M2 11h1v1H2v-1zm2 0h1v1H4v-1zm-2 2h1v1H2v-1zm2 0h1v1H4v-1zm4-4h1v1H8V9zm2 0h1v1h-1V9zm-2 2h1v1H8v-1zm2 0h1v1h-1v-1zm2-2h1v1h-1V9zm0 2h1v1h-1v-1zM8 7h1v1H8V7zm2 0h1v1h-1V7zm2 0h1v1h-1V7zM8 5h1v1H8V5zm2 0h1v1h-1V5zm2 0h1v1h-1V5zm0-2h1v1h-1V3z">
                      </path>
                    </g>
                    </svg>
                </span>
                {{ job.company }}
              </p>

              <p class="me-5 d-flex">
                <span class="me-1 pb-2"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em"
                    focusable="false" role="img" aria-label="geo alt" xmlns="http://www.w3.org/2000/svg"
                    fill="currentColor" class="bi-geo-alt b-icon bi">
                    <g data-v-378c8849="">
                      <path
                        d="M12.166 8.94c-.524 1.062-1.234 2.12-1.96 3.07A31.493 31.493 0 0 1 8 14.58a31.481 31.481 0 0 1-2.206-2.57c-.726-.95-1.436-2.008-1.96-3.07C3.304 7.867 3 6.862 3 6a5 5 0 0 1 10 0c0 .862-.305 1.867-.834 2.94zM8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10z">
                      </path>
                      <path d="M8 8a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 1a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"></path>
                    </g>
                    </svg>
                </span>
                {{ job.tipo }}
              </p>
              
            <p class="me-5">
              <span class="me-1 pb-2"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="cash" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-cash b-icon bi"><g data-v-378c8849=""><path d="M8 10a2 2 0 1 0 0-4 2 2 0 0 0 0 4z"></path><path d="M0 4a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H1a1 1 0 0 1-1-1V4zm3 0a2 2 0 0 1-2 2v4a2 2 0 0 1 2 2h10a2 2 0 0 1 2-2V6a2 2 0 0 1-2-2H3z"></path></g></svg>
              </span>
              <div v-if="job.salario">
                {{convertirADinero(job.salario_1)}} - {{convertirADinero(job.salario_2)}} COP
              </div>
              <div v-else>Confidencial</div>
            </p>     
           
              <p class="me-5 d-flex">
                <span class="me-1 pb-2"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em"
                    focusable="false" role="img" aria-label="people" xmlns="http://www.w3.org/2000/svg"
                    fill="currentColor" class="bi-people b-icon bi">
                    <g data-v-378c8849="">
                      <path
                        d="M15 14s1 0 1-1-1-4-5-4-5 3-5 4 1 1 1 1h8zm-7.978-1A.261.261 0 0 1 7 12.996c.001-.264.167-1.03.76-1.72C8.312 10.629 9.282 10 11 10c1.717 0 2.687.63 3.24 1.276.593.69.758 1.457.76 1.72l-.008.002a.274.274 0 0 1-.014.002H7.022zM11 7a2 2 0 1 0 0-4 2 2 0 0 0 0 4zm3-2a3 3 0 1 1-6 0 3 3 0 0 1 6 0zM6.936 9.28a5.88 5.88 0 0 0-1.23-.247A7.35 7.35 0 0 0 5 9c-4 0-5 3-5 4 0 .667.333 1 1 1h4.216A2.238 2.238 0 0 1 5 13c0-1.01.377-2.042 1.09-2.904.243-.294.526-.569.846-.816zM4.92 10A5.493 5.493 0 0 0 4 13H1c0-.26.164-1.03.76-1.724.545-.636 1.492-1.256 3.16-1.275zM1.5 5.5a3 3 0 1 1 6 0 3 3 0 0 1-6 0zm3-2a2 2 0 1 0 0 4 2 2 0 0 0 0-4z">
                      </path>
                    </g>
                    </svg>
                </span>
                {{ job.vacantes }}
                <div v-if="job.vacantes">&nbsp;&nbsp;Vacantes</div>
                <div v-else>Vacante</div>
              </p>

              <p class="me-5 d-flex">
                <span class="me-1 pb-2"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em"
                    focusable="false" role="img" aria-label="calendar3" xmlns="http://www.w3.org/2000/svg"
                    fill="currentColor" class="bi-calendar3 b-icon bi">
                    <g data-v-378c8849="">
                      <path
                        d="M14 0H2a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zM1 3.857C1 3.384 1.448 3 2 3h12c.552 0 1 .384 1 .857v10.286c0 .473-.448.857-1 .857H2c-.552 0-1-.384-1-.857V3.857z">
                      </path>
                      <path
                        d="M6.5 7a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2z">
                      </path>
                    </g>
                    </svg>
                </span>
                {{ job.day }} days
              </p>

              <p class="me-5 d-flex">
                <span class="me-1 pb-2">
                  <button disabled type="button" class="btn btn-outline-secondary py-0 px-2 rounded-pill">
                    Ver más
                  </button>
                </span>
              </p>
              
            </div>
          </div>

          <div v-show="ver[indice]">
            <!-- Ver más. -->
            <p class="mt-2" v-if="job.see_description">{{ job.description }}</p>
          </div>
          
        </div>
        
      </div>
    </div>
  </div>

</template>

<style scoped>
  #cartas p {
    font-size: 14.4px;
    font-family: 'Montserrat', 'Roboto', 'sans-serif';
    color: #212529;
    font-weight: 500;
  }
  
  #card-title {
    color: #343a40 !important;
  }
  
  #cartas button {
    font-size: 0.8em;
    color: #343a40 !important;
    height: 21px !important;
    width: 90px
  }
  
  #cartas {
    height: 100px;
  }
  
  div#cartas:hover {
    border: none !important;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  }
</style>
