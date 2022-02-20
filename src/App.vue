<template>
  <div>
    <h1>{{ titulo }}</h1>

    <ul>
      <li v-for="foto of fotos" :key="foto.titulo">
        <img :src="foto.url" :alt="foto.titulo">
      </li>
    </ul>

    <Variaveis/>
    <Button/>
  </div>
</template>

<script>
import Variaveis from "./Variaveis.vue"
import \button from "./Button.vue"

export default {
  components: {
    Variaveis,
    Button
  },

  data() {

    return {

      titulo: 'Alurapic', 
      fotos: []
    }
  },
  created( ) {
    
    this.$http.get('http://localhost:3000/v1/fotos')
      .then(res => res.json())
      .then(fotos => this.fotos = fotos, err => console.log(err));
    }
}



</script>

<style>
</style>
