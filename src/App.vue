
<template >
  <div class="app1" >
    <template v-if="incioLog">
      <v-app>
        <nav-drawer :state.sync="drawer" />
        <nav-bar @nav-btn-click="drawer = true" />
        <v-content class="background">
          <v-container fluid>
            <router-view />
          </v-container>
        </v-content>
      </v-app>
    </template>
    <template v-else  >
      <v-app class="main-cotainer"  >
        <v-content class="app1">
          <v-card   class="form-container">
            <v-img
              class="white--text align-end"
              height="30%"
              src="https://picsum.photos/1920/1080?random"
            >
            </v-img>
            <v-card-text class="text--primary">
              <v-form
                ref="form"
                v-model="valid"
                lazy-validation
              >
              <v-row>
                <v-col
                  cols="12"
                >
              <v-text-field
                v-model="name"
                label="Correo Electronico"
                dense
                outlined
                required
                :rules="emailRules"
              ></v-text-field>
              </v-col>
              </v-row>
              <v-row>
                <v-col
                  cols="12"
                >
                <v-text-field
                  v-model="password"
                  :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                  :type="show1 ? 'text' : 'password'"
                  name="input-10-1"
                  label="Contraseña"
                  dense
                  outlined
                  @click:append="show1 = !show1"
                  :rules="passRules"
                  required
                ></v-text-field>
              </v-col>
            </v-row>
            </v-form>
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn  text @click="snackbar = true, validate()">
                Iniciar Sesion
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-content>
      </v-app>
    <v-snackbar
      v-model="snackbar"
      :timeout="2000"
      absolute
      top
    >
      Error! Credenciales invalidas.

      <template v-slot:action="{ attrs }">
        <v-btn
          color="blue"
          text
          v-bind="attrs"
          @click="snackbar = false"
        >
          x
        </v-btn>
      </template>
    </v-snackbar>
    </template>
  </div>
</template>

<script>

import nav_bar from "@/components//nav-bar.vue"
import nav_drawer from "@/components//nav-drawer.vue";

export default {
  name: 'App',
  components: {
    "nav-drawer": nav_drawer,
    "nav-bar": nav_bar
  },
  methods: {
      validate () {
        this.$refs.form.validate()
      },
      
    },
  data: () => ({
    drawer: false,
    incioLog: false,
    show1: false,
    password: "",
    snackbar: false,
    valid: true,
    name: '',
    emailRules: [
        v => !!v || 'Este campo es requerido',
        v => /.+@.+\..+/.test(v) || 'E-mail debe ser valido'
      ],
    passRules: [
        v => !!v || 'Este campo es requerido'
      ],
  })
}
</script>


<style>
#app {
  font-family: Inter var,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,Apple Color Emoji,Segoe UI Emoji,Segoe UI Symbol,Noto Color Emoji;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333333;
  height: 100%;
}
.app1 {
  text-align: center;
  color: #333333;
  height: 100%;
  position: relative;
  background-image: url('~@/assets/cajasLog.png');
  background-size: 100% 100%;
  background-repeat: no-repeat;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}


.background-container{
  background-image: url("https://mail.google.com/mail/u/0?ui=2&ik=f80c10f487&attid=0.1&permmsgid=msg-a:r-1480230921783065295&th=177be8d3f00e4a8b&view=fimg&sz=s0-l75-ft&attbid=ANGjdJ_kyOBM3Bv2-yW4VcEBMVYcu0X645ikduIUZg5QCwXvueP4Y879e30CltqWhAQ8qO61xuV7vndOw4V_y5X6dP6mCBdXZHSkcKbRAEZ83PBQi_iEhLeU7ykhUN8&disp=emb&realattid=ii_kldgmili0");
}

.main-container {
  display: flex;
  justify-content: center;

}

.form-container {
  margin-left: 20%;
  margin-right: 20%;
  margin-top: 10%;
  height: 50%;
  max-height: 720px;
  weight: 10%;
  max-weight: 720px;
}


@media screen and (min-width:1200px){

.form-container {
  margin-left: 35%;
  margin-right:35%;
  margin-top: 10%;
  height: 400px;
  max-height: 500px;
  weight: 100px;
}                        

}

</style>

