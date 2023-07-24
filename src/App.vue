<script setup>
import { ref } from 'vue'
import HelloWorld from '@/components/HelloWorld.vue'

const msg = ref('Hello World!')
</script>

<template>
  <input v-model="msg">

  <HelloWorld :msg="msg" />
</template>