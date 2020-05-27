<template>
  <div id="servicios">
    <div v-for="(especialidad,i) in staff" :key="i">
      <div class="servicio prof" @click="toggleItem(i)">
        <h2 class="uppercase green">{{especialidad.especialidad}} +</h2>
        <div class="detalle" :class="{active : i=== activeItem}" >
          <div v-for="(item, x) in especialidad.profesionales" :key="x">
            {{ item.name }}
            <span v-for="direccion in item.address" :key="direccion"> | {{ direccion }}</span>
            <span v-if="item.action"> | </span>
            <a href="ingresar" title="turnos" v-if="item.action">Solicitar Turno</a>
            <div class="clear"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profesionales",
  methods: {
    toggleItem(i){
      this.activeItem = i != this.activeItem ? i : null;
    }
  },
  data: function() {
    return {
      activeItem: null,
      staff: [
        {
          especialidad: "ANATOMÍA PATOLÓGICA",
          profesionales: [
            {
              name: "Dra. Maldonado Mariela",
              address: ["Av. Independecia 3650"],
              action: true
            }
          ]
        },
        {
          especialidad: "CARDIOLOGÍA ADULTOS",
          profesionales: [
            {
              name: "Dr. Brown, Luciano",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dr. González, Horacio",
              address: ["Rawson 1774"],
              action: true
            },
            {
              name: "Dra. Petrucci, María Fernanda",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dra.Ranchi, Rosana ",
              address: ["Av. Tejedor 264"],
              action: true
            }
          ]
        },
        {
          especialidad: "CARDIOLOGÍA PEDIÁTRICA",
          profesionales: [
            {
              name: "Dr. Andrés, Lucas",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr.Hozbor, Andrea",
              address: ["San Luis 2143", "San Luis 2453"],
              action: true
            }
          ]
        },
        {
          especialidad: "CIRUGÍA ADULTOS",
          profesionales: [
            {
              name: "Dr. Actis, Nicolás",
              address: ["San Luis 2176"],
              action: true
            }
          ]
        },
        {
          especialidad: "CIRUGÍA PEDIÁTRICA",
          profesionales: [
            {
              name: "Dr.Dramis, Matías ",
              address: ["San Luis 2143", "Av. Tejedor 264", "Garay 2239"],
              action: true
            },
            {
              name: "Dr.Kogan, Andrés ",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr. Yamahachi, Claudio",
              address: ["San Luis 2143"],
              action: true
            }
          ]
        },
        {
          especialidad: "CIRUGÍA PLÁSTICA	",
          profesionales: [
            {
              name: "Dra. Albarenque, Gabriela",
              address: ["Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dr.Boix, Andrés ",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dr.Parellada, Ernesto",
              address: ["Av. Tejedor 264"],
              action: true
            }
          ]
        },
        {
          especialidad: "CLÍNICA MÉDICA ADULTOS",
          profesionales: [
            {
              name: "Dr. Barretto, Mariano",
              address: ["San Luis 2143", "Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Rubiolo, Natalia",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dra. Vezzozzi, Viviana",
              address: ["San Luis 2176"],
              action: true
            }
          ]
        },
        {
          especialidad: "DERMATOLOGÍA",
          profesionales: [
            {
              name: "Dra. Acosta, Marianela",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dra. Stepa, Tatiana",
              address: ["San Luis 2176", "Av. Tejedor 264"],
              action: true
            }
          ]
        },
        {
          especialidad: "FONOAUDIOLOGÍA",
          profesionales: [
            {
              name: "Fga. Bauso, Carina	",
              address: ["San Luis 2176", "Av. Tejedor 264"],
              action: true
            },
            {
              name: "Fga. Canido Vallejos, Marcia	",
              address: ["San Luis 2176"],
              action: true
            }
          ]
        },
        {
          especialidad: "GASTROENTEROLOGÍA ADULTOS",
          profesionales: [
            {
              name: "Dr. Capriotti, Andrés",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr.Conosciutto, Juan Ignacio",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr.Rastelli, Laureano",
              address: ["San Luis 2143"],
              action: true
            }
          ]
        },
        {
          especialidad: "GINECOLOGÍA Y OBSTETRICIA",
          profesionales: [
            {
              name: "Dr.Amestoy, Julio",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dra.Carrión, Rocío",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Ilarregui, Ignacio",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Landi, Guillermo",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Lopez, Sebastián",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dra.Machado, Carmen",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dra.Mattioli, Susana",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Oddone, Fabrizio",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Pérez Staracci, Andrés",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Pirrotta, Néstor",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dra.Ponce Traverso, Jorgelina",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Quaglia, Horacio",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Rossini, Mariano",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Scafetto, Fabián",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dra.Segura, Agustina",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            },
            {
              name: "Dr.Simonetti, José",
              address: ["20 de Septiembre 1538", "Las Heras 3113"]
            }
          ]
        },
        {
          especialidad: "HEMATOLOGÍA",
          profesionales: [
            {
              name: "Dr.García, Carlos Alen",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dr.García, Santiago Antuel",
              address: ["San Luis 2176", "Av. Tejedor 264"],
              action: true
            }
          ]
        },
        {
          especialidad: "INFECTOLOGÍA ADULTOS	",
          profesionales: [
            {
              name: "Dra. Bechini, Florencia	",
              address: ["San Luis 2143"],
              action: true
            }
          ]
        },
        {
          especialidad: "INMUNOLOGÍA",
          profesionales: [
            {
              name: "Dr. Uriarte, Ignacio	",
              address: ["San Luis 2176"],
              action: true
            }
          ]
        },
        {
          especialidad: "KINESIOLOGÍA",
          profesionales: [
            {
              name: "Klgo. Etcheto, Eduardo",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Klga. Panero, Gloria",
              address: ["San Luis 2143"],
              action: false
            }
          ]
        },
        {
          especialidad: "LABORATORIO",
          profesionales: [
            {
              name: "CEDEAC",
              address: ["Av. Colón 2749","San Luis 2153"],
              action: false
            }
          ]
        },
        {
          especialidad: "NEFROLOGÍA ADULTOS",
          profesionales: [
            {
              name: "Dr. Potes, Luciano",
              address: ["San Luis 2143"],
              action: true
            }
          ]
        },
        {
          especialidad: "NEUMONOLOGÍA PEDIÁTRICA",
          profesionales: [
            {
              name: "Dr. Monaldi, Guillermo",
              address: ["San Luis 2176"],
              action: true
            }
          ]
        },
        {
          especialidad: "NEUROCIRUGÍA",
          profesionales: [
            {
              name: "Dr. Aldinio, Roberto",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dra. Gorga, María Agustina",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dr. Lirussi, Pablo",
              address: ["San Luis 2143"],
              action: false
            }
          ]
        },
        {
          especialidad: "NEUROLOGÍA ADULTOS",
          profesionales: [
            {
              name: "Dra. Clement, María",
              address: ["San Luis 2143"],
              action: true
            }
          ]
        },
        {
          especialidad: "NUTRICIÓN",
          profesionales: [
            {
              name: "Lic. Grillo, Aime",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Lic. Marini, Carina",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Lic. Salemne, Alonso Marien",
              address: ["San Luis 2176"],
              action: false
            }
          ]
        },
        {
          especialidad: "NUTRICIÓN PEDIÁTRICA",
          profesionales: [
            {
              name: "Dra. Pettigrosso, Sabrina",
              address: ["San Luis 2143"],
              action: true
            }
          ]
        },
        {
          especialidad: "ODONTOLOGÍA",
          profesionales: [
            {
              name: "Dra. De Sierra, Miriam",
              address: ["San Luis 2176"],
              action: false
            },
            {
              name: "Dra. Milillo, Andrea",
              address: ["San Luis 2176"],
              action: false
            },
            {
              name: "Dr. Monteleone, Gabriel",
              address: ["San Luis 2176"],
              action: false
            },
            {
              name: "Dra. Pirro, María Fernanda",
              address: ["San Luis 2176"],
              action: false
            },
            {
              name: "Dr. Ramos, Pablo",
              address: ["San Luis 2176"],
              action: false
            }
          ]
        },
        {
          especialidad: "OFTALMOLOGÍA",
          profesionales: [
            {
              name: "Dra. Bondesio, Cristina",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dra. Giorgianni, Paula",
              address: ["San Luis 2143"],
              action: false
            }
          ]
        },
        {
          especialidad: "ORTOPEDIA Y TRAUMATOLOGÍA",
          profesionales: [
            {
              name: "Dr. Bou, Horacio",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dr. Fallesen, Pedro",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dra. Gimenez, Ivana",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr. Torcivia, José",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr. Torres, Damián",
              address: ["San Luis 2143"],
              action: false
            }

          ]
        },
        
        {
          especialidad: "OTORRINOLARINGOLOGÍA PEDIATRICA",
          profesionales: [
            {
              name: "Dr. Giménez, Antonio",
              address: ["San Luis 2143","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dr. Insaurralde, Rubén",
              address: ["San Luis 2143"],
              action: false
            },
             {
              name: "Dr. Quiroga, Victor",
              address: ["San Luis 2176"],
              action: true
            }
          ]
        },
        {
          especialidad: "OTORRINOLARINGOLOGÍA ADULTOS",
          profesionales: [
            {
              name: "Dr. Giménez, Antonio",
              address: ["San Luis 2143","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dr. Insaurralde, Rubén",
              address: ["San Luis 2143"],
              action: false
            }
          ]
        },
        {
          especialidad: "PEDIATRÍA ESPECIALISTA",
          profesionales: [
            {
              name: "Dra. Aranda, Julieta",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dra. Argerich, Soledad",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dr. Argumedo, Lucas",
              address: ["San Luis 2143","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Asis, Alejandra",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dr. Camarero, Lucas",
              address: ["San Luis 2143","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Camerano, Patricia",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dra. Cortina, Tatiana",
              address: ["San Luis 2176","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dr. Del Rio, Germán",
              address: ["San Luis 2176","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dr. Di Cicco, Roberto",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dra. Esquivel, Gabriela",
              address: ["Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dr. Falcone, Roberto",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr. Falcone, Roberto",
              address: ["San Luis 2453"],
              action: false
            },
            {
              name: "Dr. Gallo, Juan",
              address: ["San Luis 2176","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Gaspari, María Paola",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr. Knollinger, Daniel",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dra. Larregui, Gisela",
              address: ["San Luis 2143","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Losada, Ana",
              address: ["San Luis 2143","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Martín, Paula",
              address: ["Gral. Paz 3251"],
              action: false
            },
            {
              name: "Dr. Onorio, Angel",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "Dr. Perino, Juan",
              address: ["San Luis 2176","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Siro, Florencia",
              address: ["Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dra. Torres, Amarilis",
              address: ["San Luis 2143","Av. Tejedor 264"],
              action: true
            },
            {
              name: "Dr. Villar, Mario",
              address: ["San Luis 2143"],
              action: true
            },
            {
              name: "Dr. Villar, Mario",
              address: ["Bautista 120 of. 8 - Sierra de los Padres"],
              action: false
            }


          ]
        },
        {
          especialidad: "PSICOLOGÍA",
          profesionales: [
            {
              name: "Lic. Abrego, Andrea",
              address: ["San Luis 2176"],
              action: false
            },
          ]
        },


        {
          especialidad: "PSICOPEDAGOGÍA",
          profesionales: [
            {
              name: "Lic. Balzola, Gabriela",
              address: ["San Luis 2176"],
              action: false
            },
          ]
        },


{
          especialidad: "TERAPIA OCUPACIONAL",
          profesionales: [
            {
              name: "T.Ocup. Arias, Lucrecia",
              address: ["San Luis 2143"],
              action: false
            },
            {
              name: "T.Ocup. Salinas, Maria",
              address: ["San Luis 2143"],
              action: false
            },
          ]
        },


        {
          especialidad: "UROLOGÍA",
          profesionales: [
            {
              name: "Dr. Álvarez, Juan Manuel",
              address: ["Bolivar 3676"],
              action: false
            },
            {
              name: "Dr. Menéndez, Nicolás",
              address: ["San Luis 2176"],
              action: true
            },
            {
              name: "Dr. Menéndez, Nicolás",
              address: ["Bolivar 3676"],
              action: false
            },
          ]
        },




      ]
    };
  }
};
</script>

<style>
.active { 
  display: block !important;
}
@import "http://cnym.com.ar/css/grid.css";
@import "http://cnym.com.ar/css/style.css";
</style>