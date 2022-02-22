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
  margin-top: 5em;
  position: relative;
  width: 100%;
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
  font-size: 0.8em;
  color: #828282;
  letter-spacing: 0.01em;
  text-align: center;
  letter-spacing: 0.01em;
}

</style>