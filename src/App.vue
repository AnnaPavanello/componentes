<script setup>
import ButtonChild from './components/ButtonChild.vue';

function mensagemBotao(texto){
  alert(`O botão clicado foi ${texto}!`)
}
</script>

<template>
<div class="container">
  <div>
    <button class="btn btn-novo">Novo</button>
    <button class="btn btn-editar">Editar</button>
    <button class="btn btn-salvar">Salvar</button>
    <button class="btn btn-cancelar">Cancelar</button>
    <button class="btn btn-excluir">Excluir</button>
  </div>
  <div>
    <ButtonChild :tipo="'btn'" :acao="'btn-novo'" :nome="'Novo'" @clique="mensagemBotao">Novo</ButtonChild>
    <ButtonChild :tipo="'btn'" :acao="'btn-editar'" :nome="'Editar'" @clique="mensagemBotao">Editar</ButtonChild>
    <ButtonChild :tipo="'btn'" :acao="'btn-salvar'" :nome="'Salvar'" @clique="mensagemBotao">Salvar</ButtonChild>
    <ButtonChild :tipo="'btn'" :acao="'btn-cancelar'" :nome="'Cancelar'" @clique="mensagemBotao">Cancelar</ButtonChild>
    <ButtonChild :tipo="'btn'" :acao="'btn-excluir'" :nome="'Excluir'" @clique="mensagemBotao">Excluir</ButtonChild>

  </div>
</div>
</template>

<style scoped>
.btn{
  background-color: gray;
  color: white;
  border-radius: 5px;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  margin: 1px;
}
.btn-novo{
  background-color: aqua;
  color: black;
}
.btn-editar{
  background-color: yellow;
  color: black;
}
.btn-salvar{
  background-color: green;
}
.btn-cancelar{
  background-color: orange;
}
.btn-excluir{
  background-color: red;
}
</style>
