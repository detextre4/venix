<template>
  <section>
    <aside>
      <a href="https://twitter.com/venixnft?s=11" target="_blank">
        <svg-icon type="mdi" :path="path" class="icono" />
      </a>
    </aside>
    <aside>
      <span>© Copyrights VENIX | All Rights Reserved</span>
    </aside>
  </section>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon'
import { mdiTwitter } from '@mdi/js'

export default {
  name: 'Footer-cuerpo',
    components: {
      SvgIcon
    },

    data() {
      return {
        path: mdiTwitter,
      }
    }
}
</script>

<style scoped>
section {
  position: relative;
  width: 100%;
  height: 15%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
section aside:nth-child(1) {
  margin: 0em;
}
.icono {
  color: black;
  width: 90%;
  margin-bottom: 1em;
}
span {
  font-size: 0.9em;
  color: #828282;
  letter-spacing: 0.01em;
  text-align: center;
  letter-spacing: 0.01em;
}

@media (max-width: 1280px) {
  section {
  margin-top: 3%;
  }
}

@media (max-width: 912px) {
  section {
  margin-top: 5%;
  }
}
@media (max-width: 700px) {
  section {
  margin-top: 2%;
  }
}

@media (width: 540px) and (height: 720px) {
  section {
    margin-top: 2em !important;
  }
}

@media (max-width: 414px) {
  section {
    font-size: 15px;
    margin-top: 2em !important;
  }
}


@media (max-width: 300px) {
  section {
    font-size: 13px;
  }
  span {
    text-align: center;
  }
  section {
    margin-top: 3em;
  }
}
</style>