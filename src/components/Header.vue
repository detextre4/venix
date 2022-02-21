<template>
  <section>
    <aside>
        <img width="48.42" height="48.42" src="@/assets/logo2.png" alt="Logo">
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
aside {
  /* Auto layout */

  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 0px;

  position: absolute;
  width: 222.58px;
  height: 48.42px;
  left: 608.61px;
  top: 52.25px;
}
aside h2 {
    /* VENIX */


  position: static;
  width: 165.17px;
  height: 39.97px;
  left: 57.42px;
  top: 0px;

  font-family: 'Brolink', sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 44.1262px;
  line-height: 49px;

  color: #161616;


  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 9px;
}

img {
  /* Rectangle 1 */


  position: absolute;
  width: 48.42px;
  height: 48.42px;
  left: 0px;
  top: 0px;

  background: #000000;
  border-radius: 4.90291px;
}
</style>
