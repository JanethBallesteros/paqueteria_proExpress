<template>
  <v-app-bar
    v-if="$vuetify.breakpoint.mdAndDown"
    color="#222831"
    absolute
    :dense="$vuetify.breakpoint.smAndDown"
    dark
    app
  >
    <v-app-bar-nav-icon
      @click="$emit('nav-btn-click', $event)"
    ></v-app-bar-nav-icon>
    <v-toolbar-title class="app-title">Paqueteria
    </v-toolbar-title>
    <v-spacer></v-spacer>
  </v-app-bar>
</template>

<script>
export default {};
</script>

<style scoped></style>
