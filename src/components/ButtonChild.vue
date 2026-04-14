<script setup>
    defineProps(['nome', 'tipo', 'acao'])
    const emit = defineEmits(['clique'])
</script>

<template>
    <button :class="[tipo, acao]" @click.prevent="$emit('clique', nome)">
        <slot></slot>
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
.btn-editar{
  background-color: yellow;
  color: black;
}
</style>