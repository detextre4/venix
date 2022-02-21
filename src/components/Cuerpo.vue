<template>
  <section>
    <aside>
      <h1>WEN?</h1>
    </aside>

    <aside>
      <div class="imagen">
        <img width="160" height="140" src="@/assets/rana.png" alt="Image" />
      </div>
      <div class="texto">
        <h2>We are<br />Coming Soon.</h2>
        <p class="arriba"><strong>Get notified when we launch</strong></p>
        <!-- formulario -->
        <form action="" @submit.prevent="guardar">
          <input
            id="emails-input"
            v-model="form.email"
            placeholder="Email"
            type="email"
            required
          />
          <input type="submit" value="Subscribe" @submit.prevent="guardar" />
        </form>
        <!-- formulario -->
        <p class="abajo">Are you going to launch a collection on NEAR? 
          <a href="mailto:contact@venix.vision" target="_blank"><strong>Contact Us</strong></a>
        </p>
      </div>
    </aside>
  </section>
</template>

<script>
import axios from "axios";
export default {
  name: "Cuerpo-app",
  data() {
    return {
      form: {
        email: "",
        token: "",
      },
    };
  },
  methods: {
    guardar() {
      document.getElementById("emails-input").validEmails;
        axios.post('https://venix.vision/venix/apis/v1/mail/', this.form).then((response) => {
          if (response.data !== null) {
            this.form.email = '';
            alert("mail has been sent successfully ")
          }
        }
      )
    }
  },
};
</script>

<style scoped>
section {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 0;
}
aside:nth-child(1) {
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
aside:nth-child(2) {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
}
aside h1 {
  font-size: 14em;
  margin: 0;
  color: transparent;
  -webkit-text-stroke: 1px #ff6b3b;
  -moz-text-stroke: 1px #ff6b3b;
  letter-spacing: 0.01em;
}

/*/////////////////////////////////////////////// */

.imagen {
  float: left;
  margin-right: 3em;
}
.texto {
  display: inline-block;
}
.texto h2 {
  margin-top: 0;
  margin-bottom: 20px;
  font-size: 2em;
  font-weight: bold;
  -webkit-text-stroke: 0.2px #000000;
  -moz-text-stroke: 0.2px #000000;
  letter-spacing: 0.01em;
}
.arriba {
  font-family: 'Poppins', sans-serif !important;
  margin-top: 0;
  margin-bottom: 5px;
  font-size: 0.8em;
  font-weight: bold;
  -webkit-text-stroke: 0.2px #000000;
  -moz-text-stroke: 0.2px #000000;
  letter-spacing: 0.01em;
}
.abajo {
  font-size: 0.8em;
}
strong {
  color: black;
}
a {
  text-decoration-color: rgba(128, 128, 128, 0.856);
  text-decoration-thickness: 2px;
  -webkit-text-decoration-thickness: 2px;
  -moz-text-decoration-thickness: 2px;
}
input:nth-child(1) {
  text-indent: 1em;
  font-family: 'Poppins', sans-serif !important;
  font-size: 0.8em;
  width: 16em;
  height: 2.2em;
  box-shadow: 0 0 2px gray;
  border: none;
  border-color: steelblue;
  border-width: 1px;
  border-radius: 0.375em 0em 0em 0.375em;
  border-right: transparent;
  letter-spacing: 0.01em;
}
input:nth-child(2) {
  font-family: 'Poppins', sans-serif !important;
  font-weight: 550;
  font-size: 0.8em;
  color: white;
  background: #161616;
  width: 7em;
  height: 2.5em;
  border-radius: 0em 0.375em 0.375em 0em;
  border-color: transparent;
  letter-spacing: 0.01em;
  z-index: 3;
}
.decoracion {
  color: black;
}

@media (width: 360px) and (height: 740px) {
  section {
    margin-top: 1em !important;
  }
  .imagen {
    margin: auto 8em !important;
  }
}

@media (width: 375px) and (height: 667px) {
  section {
    margin-top: 0 !important;
  }
}

@media (width: 540px) and (height: 720px) {
  section {
    margin-top: 3em !important;
  }
  .imagen {
    margin: auto !important;
  }
  h1 {
    font-size: 21vmax !important;
  }
}

@media (max-width: 1280px) {
  aside:nth-child(2) {
    margin: auto;
    width: auto;
  }
}

@media (max-width: 1000px) {
  section {
    margin-top: 10%;
    font-size: 20px;
  }
  aside:nth-child(2) {
    display: block;
    margin: auto;
    width: auto;
  }
}

@media (max-width: 820px) {
  section {
     margin-top: 4em;
  }
  .imagen {
    display: block;
    justify-content: center;
    align-items: center;
    margin: auto;
  }
  img {
    width: 240px;
    height: 200px
  }
  input:nth-child(1) {
    width: 50%;
  }
}
@media (max-width: 768px) {
  section {
    font-size: 18px;
     margin-top: 4em;
  }
  .imagen {
    display: block;
    justify-content: center;
    align-items: center;
    margin: auto;
  }
  img {
    width: 230px;
    height: 180px
  }
  input:nth-child(1) {
    width: 50%;
  }
}

@media (max-width: 700px) {
  aside h1 {
    font-size: 15vmax;
  }
  section {
    font-size: 12px;
    margin-top: 0em;
  }
  aside:nth-child(2) {
    text-align: center;
  }
  .imagen {
    float: top;
    margin: auto 10em;
  }
  img {
    width: 150px;
    height: 120px
  }
  .texto h2 {
    font-size: 3em;
  }
  input:nth-child(2) {
    width: 7em;
  }
}

@media (width: 412px) and (height: 914px) {
  section {
    margin-top: 4em !important;
  }
}


@media (max-width: 414px) {
  section {
    margin-top: 4em;
  }
  input:nth-child(1) {
    width: 18em;
  }
}

@media (max-width: 300px) {
  section {
    font-size: 10px;
    margin-top: 2em;
  }
  aside h1 {
    font-size: 13vmax;
  }
  aside {
    width: 100%;
  }
  .imagen {
    float: top;
    margin: auto 8em;
  }
  img {
    width: 140px;
    height: 110px;
  }
  .texto {
    display: block;
  }
}
</style>
