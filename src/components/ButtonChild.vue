<script setup>
    defineProps(['nome', 'tipo', 'acao'])
</script>

<template>
    <button :class="[tipo, acao]">
        {{ nome }}
    </button>
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
</style>