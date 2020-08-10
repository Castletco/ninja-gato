<template>
  <b-container>
    <div>
      <b-button @click="showCat()">Display Cat</b-button>
      <b-button @click="showNinja()" variant="outline-primary">Display Ninja</b-button>
    </div>
    <div>
      <!-- <b-img-lazy v-bind="mainProps" :src="getImageUrl()" alt="Test Image"></b-img-lazy> -->
      <img :style="imagenStyle" id="cat" alt="silvester" v-bind="mainProps" :src="imagen" />
      <!-- <img id="ninja" alt="ninja" v-bind="mainProps" src="../assets/ninja.png" /> -->
    </div>
  </b-container>
</template>

<script>
  export default {
    name: 'NinjaGato',
    data() {
      return {
        gato: "../assets/silvester.png",
        ninja: "../assets/ninja.png",
        imagen: "",
        imagenStyle: "display:none",
        mainProps: {
          center: true,
          fluidGrow: true,
          blank: true,
          blankColor: '#bbb',
          width: 250,
          height: 150,
          class: 'my-5'
        }
      }
    },
    methods: {
      showCat () {
        alert("La imagen está a punto de cambiar");
        this.imagen = this.gato;
        this.imagenStyle = "";
      },
      showNinja () {
        alert("La imagen está a punto de cambiar");
        this.imagen = this.ninja;
        this.imagenStyle = "";
      },
      visibilidadImagen() {
        if (this.imagen == "") {
          return "display: none";
        } else {
          return "";
        }
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
