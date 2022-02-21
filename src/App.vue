<template>
  <div id="app">
    <Cuerpo></Cuerpo>
  </div>
</template>

<script>
import Cuerpo from '@/components/Cuerpo.vue'

export default {
  name: "App",
  components: {
    Cuerpo
  }
}
</script>

<style>
@font-face {
  font-family: 'Brolink', sans-serif;
  src: url('./assets/Brolink.otf');
}
#app {
  font-family: 'Inter', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: auto;
  max-width: 1440px;
  max-height: 1024px;
}
.header {
  flex: 0 0 auto;
}
.cuerpo {
  flex: 1 0 auto;
}
.footer {
  flex: 0 0 auto;
}
</style>
