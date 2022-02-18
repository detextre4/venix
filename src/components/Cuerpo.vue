<template>
  <section>
    <aside>
      <h1>20<sup>d</sup> 13<sup>h</sup> 26<sup>m</sup></h1>
    </aside>

    <aside>
      <div class="imagen">
        <img width="250" height="210" src="@/assets/rana.png" alt="Image" />
      </div>
      <div class="texto">
        <h2>We are<br />Coming Soon.</h2>
        <p class="arriba"><strong>Get notified when we launch</strong></p>
        <!-- formulario -->
        <form action="" @submit.prevent="guardar">
          <input
            v-model="form.email"
            placeholder="Email"
            type="email"
            pattern=".+@gmail.com"
            required
          />
          <input type="submit" value="Subscribe" @submit.prevent="guardar" />
        </form>
        <!-- formulario -->
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
      axios.post('http://157.230.2.213:85/venix/apis/v1/mail/', this.form).then((response) => {
        if (response.data !== null) {
          this.form.email = '';
          alert("mail has been sent successfully ")
        }
      })
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
}
aside:nth-child(1) {
  margin: auto;
}
aside:nth-child(2) {
  margin: auto;
  width: 60%;
}
aside h1 {
  font-size: 20vmax;
  margin: 0;
  color: transparent;
  -webkit-text-stroke: 1px #ff6b3b;
  -moz-text-stroke: 1px #ff6b3b;
}
sup {
  vertical-align: 0%;
  font-size: 0.2em;
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
  font-size: 3.4em;
  font-weight: bold;
}
p {
  font-family: 'Poppins', sans-serif !important;
  margin-top: 0;
  margin-bottom: 5px;
  font-size: 1.3em;
  font-weight: bold;
}
input:nth-child(1) {
  text-indent: 1em;
  font-family: 'Poppins', sans-serif !important;
  font-size: 1em;
  width: 21.3em;
  height: 2.65em;
  box-shadow: 0 0 2px gray;
  border: none;
  border-color: steelblue;
  border-width: 1px;
  border-radius: 0.3em 0em 0em 0.3em;
  border-right: transparent;
}
input:nth-child(2) {
  font-family: 'Poppins', sans-serif !important;
  font-weight: 600;
  font-size: 1em;
  color: white;
  background: #161616;
  width: 8em;
  height: 3em;
  border-radius: 0em 0.4em 0.4em 0em;
  border-color: transparent;
  z-index: 3;
}
.decoracion {
  color: black;
}

@media (width: 375px) and (height: 667px) {
  section {
    margin-top: 0 !important;
  }
}

@media (max-width: 1280px) {
  aside:nth-child(2) {
    margin: auto;
    width: auto;
  }
}

@media (max-width: 1000px) {
  aside h1 {
    font-size: 14vmax;
  }
}

@media (max-width: 800px) {
  section {
    font-size: 15px;
     margin-top: 2em;
  }
  img {
    width: 220px;
    height: 180px
  }
}

@media (max-width: 700px) {
  aside h1 {
    font-size: 9vmax;
  }
  section {
    font-size: 12px;
    margin-top: 3em;
  }
  aside:nth-child(2) {
    text-align: center;
  }
  .imagen {
    float: top;
    margin: auto 8em;
  }
  img {
    width: 180px;
    height: 150px
  }
  .texto h2 {
    font-size: 3em;
  }
  input:nth-child(2) {
    width: 7em;
  }
}

@media (max-width: 300px) {
  section {
    font-size: 9px;
  }
  aside {
    width: 100%;
  }
  aside:nth-child(1) {
    margin-top: 2em;
  }
  aside h1 {
    font-size: 9vmax;
  }
  img {
    width: 150px;
    height: 120px;
  }
  .texto {
    display: block;
  }
}
</style>
