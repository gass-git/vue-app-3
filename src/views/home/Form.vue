<template>
    <section>
        Text input: 
        <input 
            v-on:input="handleInput"
            v-bind:value="textInput"
        />
        <div class="char-count">
            <strong>char count: {{ charCount }}</strong>
        </div>
        <button v-on:click="$emit('submitInput', textInput)">
            submit
        </button>
    </section>    
</template>

<script setup>
import {ref, computed, watchEffect} from 'vue'

    const textInput = ref('')
    const charCount = computed(() => {
        return textInput.value.length
    })

    function handleInput(e){
        textInput.value = e.target.value
    }
</script>

<style scoped>
    section{
        display:grid;
        place-items: center;
        border:1px solid grey;
        border-radius:8px;
        width:400px;
        height: 120px;
        padding:10px;
    }
    .char-count{
        margin:10px;
        border-radius:10px;
        background:blue;
        color:white;
        padding:2px 10px 2px 10px;
    }
</style>