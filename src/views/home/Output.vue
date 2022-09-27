<template>
    <section>
        Output:
        <div v-html="identicon" />
    </section>
</template>

<script setup>
import {computed} from 'vue'
import {toSvg} from '../../../node_modules/jdenticon'

const props = defineProps({textInput: String})

const identicon = computed(() => {
    return toSvg(props.textInput, 100)
})
</script>

<style scoped>
    section{
        padding-top:20px;
        border:1px solid grey;
        border-radius: 8px;
        width:420px;
        height:180px;
    }
    div{
        margin-top:20px;
    }
</style>
