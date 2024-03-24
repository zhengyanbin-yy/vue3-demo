<script setup>
import {ref} from 'vue'
const value1 = defineModel()
const [value2,modifiers] = defineModel('test',{
  set(newVal){
    if (modifiers.capitalize){
      return newVal.charAt(0).toUpperCase() + newVal.slice(1)
    }
    return newVal
  },
})
</script>

<template>
<input v-model="value1"/><br>
<input v-model="value2"/><br>
</template>

<style scoped>

</style>