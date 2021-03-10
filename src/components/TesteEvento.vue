<template>
  <div class="teste-evento">
    <p>{{ mensagem }}</p> <!--{{ }} mostra a variável criada no script ou uma lógica ex:1+1-->
    <button @click="deixarMaiuscula">Texto em maiúsculo</button> <!--v-on directiva mágica pode ser chamada com o @-->
  </div>
</template>
<script>
export default {
  name: 'TesteEvento',
  data() {
    return {
      mensagem: 'O rato roeu a roupa do rei de Roma'
    }
  },
  methods: { //criação de função para deixar maiúsculo, Dentro de methods estão as funções que utilizaremos no componente.
            //Cada nova função deve ser separada por uma vírgula.
    deixarMaiuscula() {
      this.mensagem = this.mensagem.toUpperCase(); //this significa que a variável mensagem está dentro deste texto
    } //toUpperCase é uma função do JS que transforma o texto em maiúscula quando atribuída na mensagem
  }
}
</script>