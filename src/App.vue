<template>
  <div id="app">
    <div class="limitador cabecalho">
      <h1 class="text-center">Conversor Binário <i class="fas fa-exchange-alt"></i> Decimal</h1>
    </div>    
    <Bin2Dec></Bin2Dec>
    <Dec2Bin></Dec2Bin>
    <div class="limitador rodape">
      <h3 class="text-center">Desenvolvido com <span class="fas fa-heart"></span> por <a href="https://www.instagram.com/sameoldcarlos">Carlos Alves</a></h3>
    </div>
  </div>
  
</template>

<script>

import Bin2Dec from './components/Bin2Dec'
import Dec2Bin from './components/Dec2Bin'

export default {
  name: 'App',
  components: {
    Bin2Dec, Dec2Bin
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background: repeating-linear-gradient(
      45deg,
      #c9c8c8,
      #c9c8c8 3px,
      #a3a3a3 3px,
      #a3a3a3 6px
    )

  }

  a, a:hover{
    color: #ffffff;
    text-decoration: none;
  }

  .limitador {
    top: 0;
    width: 100%;
    height: 80px;
    background-color: #000000;
    color: #ffffff;
    display: table;
  }

  .text-center {
    vertical-align: middle;
    text-align: center;
    display:table-cell;
    
  }

  .btn {
      margin-left: 10px;
  }

  .conversor {
      margin: 30px auto;
      padding: 20px;
      max-width: 500px;
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
      background-color: #fff;
  }

  .display-3{
    color: #0069d9;
  }

</style>
