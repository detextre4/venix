<template>
  <section>
    <aside>
      <div class="imagen">
        <img width="34" height="42" src="@/assets/logo2.png" alt="Logo">
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
}
aside h2 {
  color: black;
  font-size: 2em;
  font-weight: bold;
}
.imagen {
  position: relative;
  margin-right: 0.3em;
}
img {
  border-radius: 0.4em;
}
</style>
