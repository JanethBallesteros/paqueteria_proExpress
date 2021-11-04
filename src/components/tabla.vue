<template>
  <v-container>
    <v-col cols="0" md="10">
      <v-btn
        color="Lollipop"
        @click="Agregar"
        >
        Agregar
      </v-btn>
      </v-col>
  
  <v-col cols="3" md="10">
      <v-btn
        color="Lollipop"
        @click="Agregar"
        >
        Borrar
      </v-btn>
      </v-col>
  <v-card>
    
    <div class="text-center pt-2" > <!--pt es la unidad de medida del texto-->
      
     
    </div>
    <v-card-title >
      Encargos
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
      :headers="headers"
      :items="desserts"
      :search="search"
    ></v-data-table>
  </v-card>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        search: '',
        headers: [
          {
            text: 'Tipo de encargos',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'Tipo Encargo', value: 'encargo' },
          { text: 'Fecha de Orden', value: 'dateI' },
          { text: 'Fecha Envio', value: 'dateF' },
          { text: 'Estatus', value: 'status' },
          { text: 'Paquete ID', value: 'nume' },
        ],
        desserts: [
          {
            name: 'Pedro Miguel Hernandez',
            encargo: 'Paqueteria',
            dateI: '08/08/2020',
            dateF: '02/11/2020',
            status: 'Entregado',
            nume: '15985',
            
          },
          {
            name: 'Isido José Saldaña',
            encargo: 'Pago transaccional',
            dateI: '10/07/2020',
            dateF: '02/08/2020',
            status: 'Entregado',
            nume: '12555',
          },
          {
            name: 'Gloria Belmonte Ortiz',
            encargo: 'Envío de Documentación',
            dateI: '15/08/2020',
            dateF: '17/08/2020',
            status: 'Entregado',
            nume: '1654',
          },
          {
            name: 'Pedro Miguel Hernandez',
            encargo:'Mensajería',
            dateI: '15/08/2020',
            dateF: '15/08/2020',
            status:'Entregado',
            nume: '54545',
          },
          {
            
            name: 'Maria de la Cruz Olivas Fernandez',
            encargo: 'Envío',
            dateI: '20/08/2020',
            dateF: '24/08/2020',
            status: 'Entregado',
            nume: '18794',
          },
          {
            name: 'Nora Angelica Valverde',
            encargo: 'Mensajería',
            dateI: '01/09/2020',
            dateF: '01/09/2020',
            status: 'Entregado',
            nume: '99548',
          },
          {
            name: 'Miguel Angel Murillo Sanchez',
            encargo: 'Envío',
            dateI: '04/09/2020',
            dateF: '08/09/2020',
            status: 'Entregado',
            nume: '87455',
          },
          {
            name: 'Francisco Fernando Rodulfo Montalvo  ',
            encargo: 'Pago transaccional',
            dateI: '04/09/2020',
            dateF: '04/09/2020',
            status: 'Entregado',
            nume: '8789',
          },
          {
            name: 'Luis Manuel Rivas Holague',
            encargo: 'Envío de documentación',
            dateI: '05/09/2020',
            dateF: '05/09/2020',
            status: 'Entregado',
            nume: '8752',
            
            
          },
          {
            name: 'Beatriz Angelica Ruiz Hernandez',
            encargo: 'Mensajería',
            dateI: '08/09/2020',
            dateF: '08/09/2020',
            status: 'Entregado',
            nume: '78511',
          },
        ],
      }
    },
  }
</script>

