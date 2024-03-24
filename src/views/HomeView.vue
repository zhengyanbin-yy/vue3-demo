<script setup>
import {ref,watch,watchEffect} from 'vue'
import DemoComponent from "@/components/demo_components/DemoComponent.vue";
const v1 = ref(' 1')
const v2 = ref('a')
</script>

<template>
  <div>{{v1}}</div>
  <div>{{v2}}</div>
  <demo-component v-model.trim="v1" v-model:test.capitalize="v2"></demo-component>
</template>
