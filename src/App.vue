<template>
  <div>
    <h1>{{ titulo }}</h1>

    <ul>
      <li v-for="foto of fotos" :key="foto.titulo">
        <img :src="foto.url" :alt="foto.titulo">
      </li>
    </ul>

    <Variaveis/>
    
  </div>
</template>

<script>
import Variaveis from "./Variaveis.vue"

export default {
  components: {
    Variaveis
  },

  data() {

    return {

      titulo: 'Alurapic', 
      fotos: [
        {
          url: 'https://s2.glbimg.com/nvjFq8VRjyrpdQqaOeywz-5DFwY=/e.glbimg.com/og/ed/f/original/2021/08/27/captura_de_tela_2021-08-27_as_11.01.15.png' ,
          titulo: 'cachorro'
        },
        {
          url: 'https://s2.glbimg.com/nvjFq8VRjyrpdQqaOeywz-5DFwY=/e.glbimg.com/og/ed/f/original/2021/08/27/captura_de_tela_2021-08-27_as_11.01.15.png' ,
          titulo: 'Cachorrão'
        }
      ]
    }
  }
}


</script>

<style>
</style>
