<template>
    
    <h1>{{ msg }}</h1>

</template>


<script>

    var nome = 'Rafaella'
    var sobrenome = 'Souza'
    var variaveis = nome + sobrenome

export default {
    nome: 'Variaveis',
    data() {
        return {
            msg: variaveis
        }
    }
}
</script>