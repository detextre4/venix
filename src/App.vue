<template>
  <div id="app">
    <div class="center">
      <Header></Header>
      <Cuerpo></Cuerpo>
      <Footer></Footer>
    </div>
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
@media (min-width: 1400px) {
  #app {
  width: 1440px;
  }
  section {
    font-size: 19px;
  }
}
@media (max-width: 1024px) {
  section {
    font-size: 14px;
  }
}
@media (max-width: 912px) {
  #app {
    height: auto;
  }
  .center {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  section {
    font-size: 20px;
  }
}
@media (max-width: 912px) {
  section {
    font-size: 18px;
  }
}
@media (max-width: 540px) {
  .center {
    margin-top: 30%;
  }
}
@media (max-width: 500px) {
  .center {
    margin-top: 60%;
  }
}
@media (max-width: 280px) {
  section {
    font-size: 13px;
  }
  .center {
    margin-top: 70%;
  }
}
</style>
