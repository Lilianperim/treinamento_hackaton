<template>
  <div class="sites-favoritos">
    <h2>Sites favoritos</h2>
    <ul>
      <li
        v-for="site of sitesFavoritos"
        :key="site.id"
      >
        <a :href="site.url">{{ site.nome }}</a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'SitesFavoritos',
  data() {
    return {
      sitesFavoritos: []
    }
  },
  //estrutura para API
  created() {  //função do vue vai chamar o componente somente quando ele for criado (eles são destruídos com o tempo)
    fetch('https://hackthon-decola.firebaseio.com/sites-favoritos.json')
      .then(response => response.json())//then é igual então
      .then(json => {//então pega o resultado da linha de cima e atribuia ao json a variavel sitesfavoritos
        this.sitesFavoritos = json
      })
  }
}
</script>