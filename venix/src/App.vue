<template>
  <div id="app">
    <Header></Header>
    <Cuerpo></Cuerpo>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Cuerpo from '@/components/Cuerpo.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: "App",
  components: {
    Header,
    Cuerpo,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Inter', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 1em;
  width: 100%;
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
