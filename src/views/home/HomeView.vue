<template>
  <div class="home">
    <Form v-on:console-input="consoleInput" />
    <Output />
  </div>
</template>

<script setup>
import Form from './Form.vue'
import Output from './Output.vue'

  function consoleInput(text){
    console.log(text)
  }
</script>

<style scoped>
  .home{
    display:grid;
    gap: 30px;
    grid-template-columns: auto;
    justify-content: center;
  }
</style>