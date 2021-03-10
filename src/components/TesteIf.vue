<template>
    <div class="teste-if">
        <h1 v-if="podeVer">Teste1</h1>
        <h1 v-else>Teste 2</h1>
    </div>
</template>

<script>
export default {
    name:'TesteIf',
    data() {   //Dentro de data() estão os dados que serão utilizados do próprio componente.
        return{
            podeVer: false //variável que será usada no template
        }
    }
}
</script>


<style scoped>

</style>