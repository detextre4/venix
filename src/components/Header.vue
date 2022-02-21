<template>
  <section>
    <aside>
      <div class="imagen">
        <img width="34" height="40" src="@/assets/logo2.png" alt="Logo">
      </div>
      <h2>VENIX</h2>
    </aside>
  </section>
</template>

<script>
export default {
  name: 'Header-cuerpo'
}
</script>


<style scoped>
section {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 10%;
}
aside {
  width: 15%;
  display: flex;
  align-items: center;
  justify-content: center;
  transform: scale(1.1, 0.9);
  -webkit-text-stroke: 0.5px #000000;
  -moz-text-stroke: 0.5px #000000;
}
aside h2 {
  font-family: 'Brolink', sans-serif;
  color: black;
  font-size: 2em;
  font-weight: bold;
}
.imagen {
  position: relative;
  margin-right: 0.4em;
}
img {
  border-radius: 4.90291px;
}

@media (max-width: 1000px) {
  aside h2 {
    font-size: 5em;
  }
  img {
    border-radius: 0.4em;
    width: 70px;
    height: 90px;
  }
}

@media (max-width: 1024px) {
  section {
    font-size: 14px;
  }
}
@media (max-width: 912px) {
  img {
    width: 60px;
    height: 70px;
  }
}
@media (max-width: 280px) {
  section {
    font-size: 13px;
  }
}
</style>
