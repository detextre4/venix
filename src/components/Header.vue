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

@media (max-width: 1000px) {
  section {
    margin-top: 10%;
    height: 10%;
  }
  aside h2 {
    font-size: 5em;
  }
  img {
    border-radius: 0.4em;
    width: 70px;
    height: 100px;
  }
}

@media (max-width: 820px) {
  section {
    margin-top: 9%;
    height: 7%;
  }
  aside h2 {
    font-size: 3em;
  }
  img {
    border-radius: 0.4em;
    width: 50px;
    height: 70px;
  }
}
@media (max-width: 768px) {
  section {
    margin-top: 5%;
    height: 7%;
  }
  aside h2 {
    font-size: 3em;
  }
  img {
    border-radius: 0.4em;
    width: 50px;
    height: 70px;
  }
}

@media (max-width: 500px) {
  section {
    margin-top: 5%;
    height: 7%;
  }
  aside h2 {
    font-size: 2em;
  }
  img {
    border-radius: 0.4em;
    width: 30px;
    height: 40px;
  }
}
</style>
