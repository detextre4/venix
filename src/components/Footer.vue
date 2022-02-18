<template>
  <section>
    <aside>
      <a href="https://twitter.com/venixnft?s=11" target="_blank" class="fa-brands fa-twitter"></a>
    </aside>
    <aside>
      <span>© Copyrights VENIX | All Rights Reserved</span>
    </aside>
  </section>
</template>

<script>
export default {
  name: 'Footer-cuerpo'
}
</script>

<style scoped>
section {
  position: relative;
  width: 100%;
  height: 22%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
section aside:nth-child(1) {
  margin: 0em;
}
aside:nth-child(1) a {
  margin: 0.5em;
  color: black;
  background: transparent;
  font-size: 1.3em;
  text-decoration: none;
}
section aside:nth-child(2) {
  margin: 1em;
}
span {
  color: #828282;
  letter-spacing: 0.01em;
}

@media (min-width: 1380px) {
  section {
  margin-top: 4%;
  }
}
@media (max-width: 1280px) {
  section {
  margin-top: 0%;
  }
}

@media (max-width: 900px) {
  section {
  margin-top: 5%;
  }
}
@media (max-width: 700px) {
  section {
  margin-top: 0%;
  }
}

@media (width: 540px) and (height: 720px) {
  section {
    margin-top: 2em !important;
  }
}


@media (max-width: 300px) {
  span {
    text-align: center;
  }
}
</style>