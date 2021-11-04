<template>
  <div id="Home">
    <div class="Home">
      <!--- <h1>prueba de todossssssssssssssssssssssssss
    </h1>-->
      <Prueba  />
      <Grafic msg="jfhjd"/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Prueba from "@/components/ControlUsersSize.vue";
import Grafic from "@/components/graficas.vue";

export default {
  name: "Home",
  components: {
    Prueba,
    Grafic,
  },
};
</script>

<!--<style>
#Home {
  font-family: Inter var, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI,
    Roboto, Helvetica Neue, Arial, Noto Sans, sans-serif, Apple Color Emoji,
    Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333333;
  height: 100%;
}
#nav {
  padding: 30px;
}

*#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

/* Scroller classes */
::-webkit-scrollbar {
  width: 8px;
}
::-webkit-scrollbar-track {
  background: #eeeeee;
  /* border-radius: 5px; */
}
::-webkit-scrollbar-thumb {
  background: #bdbdbd;
  /* border-radius: 5px; */
  transition: background 250ms ease-out;
}
::-webkit-scrollbar-thumb:hover {
  background: #bdbdbd;
}
.background {
  background-image: url("https://i.pinimg.com/originals/85/7f/f1/857ff107a3544b180bbeacc04c028806.jpg");
}

.background:before {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  height: 0%;
  z-index: -1;
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  background-position: top left;
  background-repeat: repeat;
  background-size: auto;
  background-attachment: auto;
  border-bottom: 1px solid #eaeaeb;
}
</style>

-->
