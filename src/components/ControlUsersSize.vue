
<template>
<v-container>
  <v-col cols="0" md="10">
  <bar></bar>
  </v-col>
  <v-container>
    <!-- --><v-row class="text-center">
      <v-col cols="20" md="12">
        <imagen></imagen>
      </v-col>
    </v-row>
    <!-- -->

    <v-row class="text-center">
      <v-col cols="12" md="12">
        <v-row class="text-center">
          <!-- Card 1 -->
          <v-col cols="12" md="3">
            <cards></cards>
          </v-col>
          <!-- Card 2 -->
          <v-col cols="12" md="3">
            <cards></cards>
          </v-col>
          <!-- Card 3 -->
          <v-col cols="12" md="3">
            <cards></cards>
          </v-col>
          <!-- Card 4 -->
          <v-col cols="12" md="3">
            <cards></cards>
          </v-col>
        </v-row>
      </v-col>

      <v-col cols="12" md="12">
        <v-row class="text-center">
          <!--<v-col cols="12" md="8"> </v-col>-->
          <v-col cols="12" md="4">
            <grafica></grafica>
          </v-col>
          <v-col cols="12" md="8">
            <!-- CARRRUSEL  -->
            <carrusel></carrusel>
          </v-col>
          
        </v-row>
      </v-col>
<!--
      <v-col cols="12" md="12">
        <v-row class="text-center">
          <v-col cols="12" md="4"> </v-col>
          <v-col cols="12" md="8">
           

            <grafica></grafica>
          </v-col>
        </v-row>
      </v-col>
-->
    </v-row>
  </v-container>
  </v-container>
</template>

<script>
import cards from "@/components/cards.vue";
import carrusel from "@/components/carrusel.vue";
import imagen from "@/components/imagen.vue";
import grafica from "@/components/grafica.vue";
import bar from "@/components/bar.vue";



export default {
  name: "ControlUsersSize",
  components: {
    cards,
    carrusel,
    imagen,
    grafica,
    bar,
  },
    Graficata: () => ({}),
};
</script>
