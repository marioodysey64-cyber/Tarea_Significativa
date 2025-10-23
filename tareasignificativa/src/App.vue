<template>
  <div id="app">
    <AppNavbar></AppNavbar>
    <router-view></router-view>
    <Footer></Footer>
  </div>
</template>

<script>
import AppNavbar from './components/AppNavbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    AppNavbar,
    Footer
  }
}
</script>

<style>
/* Estilos globales */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  min-height: 100vh;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* Asegura que el contenido principal ocupe el espacio disponible */
#app > *:not(footer) {
  flex: 1;
}
</style>

