<template>
  <v-navigation-drawer
    :width="drawerWidth"
    v-model="drawerState"
    color="#222831"
    :permanent="$vuetify.breakpoint.lgAndUp"
    :bottom="$vuetify.breakpoint.mdAndDown"
    dark
    app
  >
    <div  v-if="$vuetify.breakpoint.lgAndUp" color="#cf7500">
      Menú
      <v-divider></v-divider>
    </div>
    <div v-else class="close-btn-cont">
      <v-icon class="close-btn" @click="drawerState = !drawerState"
        >mdi-close</v-icon
      >
    </div>
    <div>
      <v-list class="custom-active-color" nav expand dense>

      <v-list-item key="home" to="/">
        <v-list-item-icon>
          <v-icon>mdi-home-account</v-icon>
        </v-list-item-icon>
        <v-list-item-content class="menu-item">Home</v-list-item-content>
      </v-list-item>
      
      <v-list-item key="inicio" to="/datos">
        <v-list-item-icon>
          <v-icon>mdi-book-open-page-variant</v-icon>
        </v-list-item-icon>
        <v-list-item-content class="menu-item">Control de Usaurios</v-list-item-content>
      </v-list-item>

      <v-list-item key="about" to="/about">
        <v-list-item-icon>
          <!--   mdi-alert-circle-->
          <v-icon>mdi-clipboard-text-search</v-icon>
        </v-list-item-icon>
        <v-list-item-content class="menu-item">Informes</v-list-item-content>
      </v-list-item>
      
      <v-list-item key="regempleados" to="/regempleados"> <!-- cambiar para asignar una vista -->
        <v-list-item-icon>
          <v-icon>mdi-file-document-edit</v-icon>
        </v-list-item-icon>
        <v-list-item-content class="menu-item">Registro</v-list-item-content>
      </v-list-item>

      <v-list-item key="n" to="/dashboard"> <!-- cambiar para asignar una vista -->
        <v-list-item-icon>
          <v-icon>mdi-chart-areaspline</v-icon>
        </v-list-item-icon>
        <v-list-item-content class="menu-item">Dashboard</v-list-item-content>
      </v-list-item>

      <v-list-item key="entregas" to="/entregas"> <!-- cambiar para asignar una vista -->
        <v-list-item-icon>
          <v-icon>mdi-dolly</v-icon>
        </v-list-item-icon>
        <v-list-item-content class="menu-item">Entregas</v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>
      <v-list-item>
        <v-list-item-icon>
          <v-icon>mdi-door-closed-lock</v-icon>
        </v-list-item-icon>
        <v-list-item-content class="menu-item">Cerrar sesión</v-list-item-content>
      </v-list-item>
    </v-list>
    </div>
    <div v-if="$vuetify.breakpoint.lgAndUp">

      <v-divider></v-divider>
    </div>
  </v-navigation-drawer>

</template>

<script>



export default {
  components: {
  },
  props: {
    state: {
      type: Boolean,
      // requerido para que funcione de manera responsiva
      required: true
    }
  },
  data() {
    return {
      drawerState: false,
      drawerWidth: 250,
      item: 0,
      items: null
    };
  },
  created() {
     if (this.$width < 1700) {
       this.drawerWidth = 280;
     }
  },

  watch: {
    // state(newVal) {
    //   this.drawerState = this.state;
    // },
    // drawerState(newVal) {
    //   if (!newVal) {
    //     this.close();
    //   }
    // }
  },
  methods: {
    close() {
      this.$emit("update:state", false);
    }
  }
};
</script>

<style scoped>

.close-btn {
  height: 24px;
}

.close-btn-cont {
  height: 40px;
  padding: 8px 16px 0 0;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.extra-item-cont {
  align-items: center;
  display: flex;
  height: 40px;
  justify-content: flex-end;
  padding: 0 16px;
}

.right {
  flex: 1;
  overflow-y: scroll; /* it works! */
}

/* color del texto activo dentro del navbar */
.v-application .custom-active-color .primary--text {
  color: #2196f3 !important;
}

</style>
