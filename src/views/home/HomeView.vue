<template>
  <div class="home">
    <Form v-on:submit-input="submitInput" />
    <Output v-bind:text-input="textInput"/>
  </div>
</template>

<script setup>
import Form from './Form.vue'
import Output from './Output.vue'
import {ref} from 'vue'

  const textInput = ref('')

  function submitInput(text){
    textInput.value = text
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