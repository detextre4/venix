<template>
  <section>
    <aside>
      <h1>WEN?</h1>
    </aside>

    <aside>
      <div class="imagen">
        <img width="200" height="170" src="@/assets/rana.png" alt="Image" />
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
        <p class="abajo">
          Are you going to launch a collection on NEAR?
          <a
            href="https://twitter.com/venixnft?s=11"
            target="_blank"
            class="decoracion"
            ><strong>Contact Us</strong></a
          >
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
      axios.post('http://157.230.2.213:85/venix/apis/v1/mail/', this.form).then((response) => {
        if (response.data !== null) {
          this.form.email = ''
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
aside h1 {
  font-size: 14.5vmax;
  margin: 0;
  color: transparent;
  -webkit-text-stroke: 1px #ff6b3b;
  -moz-text-stroke: 1px #ff6b3b;
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
  font-size: 2.3em;
  font-weight: bold;
}
.arriba {
  margin-top: 0;
  -webkit-text-stroke: 0.5px black;
  -moz-text-stroke: 0.5px black;
}
input:nth-child(1) {
  width: 19em;
  height: 2em;
}
input:nth-child(2) {
  color: white;
  background: #161616;
  width: 7em;
  height: 2.5em;
  border-radius: 0.2em 0.4em 0.4em 0.2em;
  border-color: transparent;
}
.abajo {
  text-align: center;
}
.decoracion {
  color: black;
}
@media (max-width: 800px) {
  img {
    width: 150px;
    height: 150px;
  }
  .texto h2 {
    margin-top: 0.5em;
  }
  .texto {
    display: block;
  }
  .arriba {
    text-align: center;
  }
  form {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

@media (max-width: 500px) {
  .imagen {
    float: left;
    margin: 0 1em 0 1em;
  }
}

@media (max-width: 280px) {
  img {
    width: 100px;
    height: 100px;
  }
  .texto h2 {
    font-size: 4.2vmax;
    margin-top: 0.5em;
  }
  .texto {
    display: block;
  }
  .arriba {
    text-align: center;
  }
  input:nth-child(1) {
    width: 12.4em;
  }
  aside h1 {
    margin-top: 10%;
  }
}
</style>
