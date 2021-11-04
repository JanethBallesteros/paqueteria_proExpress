<template>

  <v-container>
    <barra></barra>
    <v-col cols="12" md="12">
      <v-row class="text-center">
        <v-col cols="12" md="6">
          <imagen></imagen>
        </v-col>
      </v-row>
    </v-col>
    <!-- <footer></footer> -->
    <v-row class="text-center">
      <v-col cols="12" md="12">
        <v-row class="text-center">
          <v-col cols="12" md="4">
            <v-card class="mx-auto" max-width="344" outlined>
              <v-list-item three-line>
                <v-list-item-content>
                  <div class="overline mb-4">OVERLINE</div>
                  <v-list-item-title class="headline mb-1">
                    Headline 5
                  </v-list-item-title>
                  <v-list-item-subtitle
                    >Greyhound divisely hello coldly
                    fonwderfully</v-list-item-subtitle
                  >
                </v-list-item-content>

                <v-list-item-avatar
                  tile
                  size="80"
                  color="grey"
                ></v-list-item-avatar>
              </v-list-item>

              <v-card-actions>
                <v-btn outlined rounded text> Button </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col cols="12" md="8">
            <carrusel></carrusel>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="12" md="12">
        <v-row class="text-center">
          <v-col cols="12" md="3">
            <cards></cards>
          </v-col>
          <v-col cols="12" md="3">
            <!-- Card2 -->
            <cards></cards>
          </v-col>
          <v-col cols="12" md="3">
            <!-- card1 -->
            <cards></cards>
          </v-col>
          <v-col cols="12" md="3">
            <cards></cards>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import cards from "@/components/cards.vue";
import carrusel from "@/components/carrusel.vue";
import imagen from "@/components/imagen.vue";
import barra from "@/components/barra.vue"
//import footer from "@/components/footer.vue";

export default {
  name: "HelloWorld",
  components: {
    cards,
    carrusel,
    imagen,
    barra,
    // footer,
  },
  data: () => ({}),
};
</script>
